pipeline {
    agent any
    stages {
        stage("synopsys-security-scan") {
          steps {
              	echo 'SYNOPSYS SECURITY SCAN EXECUTION STARTED'

                 script {
                     synopsys_scan product: "POLARIS", polaris_assessment_types: "SCA, SAST", polaris_application_name: "test_jenkins", polaris_project_name: "springboot-pipeline-test", polaris_server_url: "https://poc.polaris.synopsys.com/", polaris_branch_name: "main"
                }
            }
        }
    }
}
