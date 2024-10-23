pipeline {
    agent{label 'siyaram_mac'}
    stages{
        stage("Coverity Issue Check") {       
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.cnc.duckutil.net', projectName: 'coverity_test', viewName: 'Outstanding Untriaged',markUnstable: true
    }
        }
}
}
