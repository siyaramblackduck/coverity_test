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
               synopsys_scan product: 'blackduck', blackduck_automation_prcomment: true, blackduck_scan_failure_severities: "ALL"
        }
        
        stage("build") {
              echo 'BUILD EXECUTION STARTED'
              echo 'Pulling...' + env.BRANCH_NAME
       }
       
}
