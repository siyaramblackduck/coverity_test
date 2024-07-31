pipeline {
    agent any

    stages{
        stage("Coverity Issue Check") {       
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.coverity.synopsys.com/', projectName: 'Node_Goat_E2E', viewName: 'High Impact Outstanding'
                }	
        }
    }
}
