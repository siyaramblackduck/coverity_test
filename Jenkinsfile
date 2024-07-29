pipeline {
    agent any

    stages{
        stage("Coverity Issue Check") {       
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.coverity.synopsys.com/', markUnstable: false, projectName: 'test_coverity', viewName: 'Outstanding Untriaged'
                }	
        }
    }
}
