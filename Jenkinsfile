pipeline {
    agent any

    stages {
        stage("unit-test") {
            steps {
                echo 'UNIT TEST EXECUTION STARTED'
            }
        }
        stage("functional-test") {
            steps {
                echo 'FUNCTIONAL TEST EXECUTION STARTED'
            }
        }
        stage("Coverity Issue Check") {
              
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.coverity.synopsys.com/', markUnstable: true, projectName: 'bitbucket_nodejs_goof_e2e_testing', viewName: 'High Impact Outstanding'
                }	
        }
        stage("build") {
            steps {
                echo 'BUILD EXECUTION STARTED'
                echo 'Pulling...' + env.BRANCH_NAME
            }
        }
    }
}
