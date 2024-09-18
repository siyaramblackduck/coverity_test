pipeline {
    agent any

        stage("synopsys-security-scan") {
          steps {
              	echo 'SYNOPSYS SECURITY SCAN EXECUTION STARTED'

                script {

                   synopsys_scan product:'polaris', polaris_prComment_enabled: true

                }	
        }
}
}
