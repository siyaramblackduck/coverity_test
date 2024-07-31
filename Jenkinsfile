pipeline {
    agent any

    stages{
        stage("Coverity Issue Check") {       
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.coverity.synopsys.com/', markUnstable: true, projectName: 'E2E_Integrations_Project_gitlab_macos', viewName: 'My Outstanding'
                }	
        }
    }
}
