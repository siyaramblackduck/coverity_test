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
              synopsys_scan product:'blackduck',  blackduck_url: 'https://testing.blackduck.synopsys.com/'
        }
        
        stage("build") {
              echo 'BUILD EXECUTION STARTED'
              echo 'Pulling...' + env.BRANCH_NAME
       }
       
}
