pipeline {
    agent{label 'siyaram_mac'}
    stages{
        stage("Coverity Issue Check") {       
                steps {
                  coverityIssueCheck coverityInstanceUrl: 'https://integrations-qa.dev.cnc.duckutil.net', projectName: 'bitbucket_nodejs_goof_e2e_testing', viewName: 'High Impact Outstanding',markUnstable: true
    }
        }
}
}
