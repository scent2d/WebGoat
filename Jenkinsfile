node {
    timestamps {
        
        stage('[+] git clone') {
            git branch: 'develop', url: 'https://github.com/scent2d/WebGoat.git'
        }

        stage('[+] SIS(Sensitive Information Scan) phase') {
            // truffleHog

        }

        stage('[+] SIS Quality Gate') {
            
        }

        stage('[+] SAST(Static Application Security Testing) phase') {
            // Sonarqube
            
        }

        stage('[+] SAST Quality Gate') {

        }

        stage('[+] DAST(Dynamic Application Security Testing) phase') {
            // OWASP ZAP

        }

        stage('[+] DAST Quality Gate') {

        }
              
        stage('[+] SCA(Software Composition Analysis) phase') {
            sh '''
                cd webgoat-container
                /home/scent2d/tools/dependency-check/check.sh
            '''
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'webgoat-container/odc-reports', reportFiles: 'dependency-check-report.html', reportName: 'OWASP Dependency Check', reportTitles: ''])
        }

        stage('[+] SCA Quality Gate') {
            // OWASP SCA
        }

        stage('[+] Container Security phase') {
            
        }

        stage('[+] Container Quality Gate') {

        }

        stage('[+] VM(Vulnerability Management) phase') {

        }

        
        
    }
}