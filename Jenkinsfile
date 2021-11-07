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
            echo 'SCA TEST Complete'
        }
        
    }
}