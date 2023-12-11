pipeline {
    agent any
    environment {
        HTTP_PROXY = 'http://bds:blackduck@us1a-qa-ssl-proxy01.nprd.sig.synopsys.com:3130/'
        NO_PROXY = 'https://example.com,http://10.0.0.95'
    }
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
                
                synopsys_scan synopsys_security_product: 'blackduck', blackduck_url: "${env.BLACKDUCK_URL}", blackduck_api_token: "${env.BLACKDUCK_TOKEN}",
                polaris_application_name: "test_jenkins", polaris_project_name: "springboot-pipeline-test", polaris_assessment_types: "SCA",  
                synopsys_bridge_download_version: "1.0.0"
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
