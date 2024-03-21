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
               synopsys_scan product: 'coverity', coverity_automation_prcomment: true
        }
        
        stage("build") {
              echo 'BUILD EXECUTION STARTED'
              echo 'Pulling...' + env.BRANCH_NAME
       }
       
}
