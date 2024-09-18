pipeline {
    agent any
    stages {
        stage("synopsys-security-scan") {
            when {
                // Triggering Synopsys Security Scan on master branch or Pull Request
                anyOf {
                    branch 'master'
                    branch pattern: "PR-\\d+", comparator: "REGEXP"
                }
            }
            steps {
                script {
                    def status = synopsys_scan product: 'polaris',
                        // Uncomment if below parameters are not set in global configuration
                        // polaris_server_url: 'POLARIS_SERVER_URL',
                        // polaris_access_token: 'POLARIS_TOKEN', 
                        // bitbucket_token: 'BITBUCKET_TOKEN', // Used for PR comment. Use github_token for GitHub or gitlab_token for GitLab
                        // bitbucket_username:'BITBUCKET_USERNAME' // Used for bitbucket cloud pr comment if app password is set as bitbucket_token 
                            polaris_assessment_types: 'SAST,SCA',
                            polaris_prComment_enabled: true,
                            polaris_application_name: 'github_test', 
                            polaris_project_name: 'github_test'
    
                        // Pull Request Comments
    
                        // SARIF report generation
                        //  polaris_reports_sarif_create: true
                            
                        // Mark build status if issues found
                        //  mark_build_status: 'UNSTABLE'
                    
                     // Uncomment to add custom logic based on return status
                    // if (status == 8) { unstable 'policy violation' }
                    // else if (status != 0) { error 'plugin failure' }
                }
            }
        }
    }
}
