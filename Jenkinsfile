pipeline {
    agent any
    
    stages {
        stage("blackduck-security-scan") {
           steps {
               script {
                   security_scan  product: 'blackducksca', blackducksca_fixpr_enabled: true,include_diagnostics: true
                    
                }
            }           
        }
    }
}



