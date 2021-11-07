node {
    timestamps {
        
        stage('[+] git clone') {
            git branch: 'develop', url: 'https://github.com/scent2d/WebGoat.git'
        }
              
        stage('[+] SCA TEST') {
            sh '''
                cd webgoat-container
                /home/scent2d/tools/dependency-check/check.sh
            '''
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '$WORKSPACE/webgoat-container/odc-reports', reportFiles: 'dependency-check-report.html', reportName: 'OWASP Dependency Check', reportTitles: ''])
            echo 'SCA TEST Complete'
        }
        
    }
}