pipeline {
    agent any
    stages {
        stage('Sanity-check') {
            steps {
                sh 'ping google.com -c5'
            }
            steps {
                sh '''
                    for i in {1..5}
                        do
                        echo $i
                    done
                '''
            }
        }
    }
}
