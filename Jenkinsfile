pipeline {
    agent any
    // agent {
    //     label 'linux-agent'
    // }
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
                     synopsys_scan product: "POLARIS", polaris_assessment_types: "SCA, SAST", polaris_application_name: "test_jenkins", polaris_project_name: "springboot-pipeline-test", polaris_server_url: "https://poc.polaris.synopsys.com/", polaris_access_token: "rksncmk4it4av0ndrm0eq1i2u3hrhfvimmd48dsua96ov0vreeohevhutb0qt8ks47hgcf920e5pm", polaris_branch_name: "main"
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
