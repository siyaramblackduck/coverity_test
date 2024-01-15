pipeline {
    agent any
    // environment {
    //     BLACKDUCK_TRUST_CERT=true
    // }
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
        stage("synopsys-security-scan") {
          steps {
              	echo 'SYNOPSYS SECURITY SCAN EXECUTION STARTED'

                script {
                   synopsys_scan product:'blackduck', blackduck_url: env.SERVER_URL, blackduck_token: '${TOKEN}', blackduck_automation_prcomment: false, github_token: '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'
                }	
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
