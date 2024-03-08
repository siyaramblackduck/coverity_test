node {
   checkout scm
   stage("unit-test") {
            echo 'UNIT TEST EXECUTION STARTED'
        }
        stage("functional-test") {
            echo 'FUNCTIONAL TEST EXECUTION STARTED'
        }
        
       stage("synopsys-security-scan") {
              echo 'SYNOPSYS SECURITY SCAN EXECUTION STARTED'
              synopsys_scan product:'blackduck',  blackduck_url: 'https://testing.blackduck.synopsys.com/', blackduck_scan_full: false
        }
        
        stage("build") {
              echo 'BUILD EXECUTION STARTED'
              echo 'Pulling...' + env.BRANCH_NAME
       }
       
}


