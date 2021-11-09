node {
    timestamps {
        
        stage('[+] git clone') {
            git branch: 'develop', url: 'https://github.com/scent2d/WebGoat.git'
        }

        stage('[+] SIS(Sensitive Information Scan) phase') {
            // truffleHog

        }

        stage('[+] SAST(Static Application Security Testing) phase') {
            // Sonarqube
            
        }

        stage('[+] DAST(Dynamic Application Security Testing) phase') {
            // OWASP ZAP

        }
              
        stage('[+] SCA(Software Composition Analysis) phase') {
            sh '''
                cd webgoat-container
                /home/scent2d/tools/dependency-check/check.sh
            '''
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'webgoat-container/odc-reports', reportFiles: 'dependency-check-report.html', reportName: 'OWASP Dependency Check', reportTitles: ''])
        }

        stage('[+] SCA Quality Gate') {

        }

        stage('[+] Container Security phase') {
            
        }

        
        
    }
}