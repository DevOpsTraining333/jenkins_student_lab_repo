pipeline {
    agent any
    stages {
        stage('Sanity-check') {
            steps {
                sh 'ping google.com -c5'
                sh '''
                    for i in {1..5}
                        do
                        echo $i
                    done
                '''
                sh '''
                sudo yum install sshpass
                sshpass -p 000000 ssh 192.168.56.136 -l root 
                systemctl status httpd
                '''
        }
    }
}
}
