pipeline {
    agent any

    stages{
        stage("Coverity Issue Check") {       
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.coverity.synopsys.com/', projectName: 'bridge-test-vulnerable-app-gradle', viewName: 'High Impact Outstanding'
                }	
        }
    }
}
