pipeline {
    agent any

    stages {
        stage('Pull') {
                agent {
                    docker {
                        image 'node:18-alpine'
                        reuseNode true
                    }
                }
            
            steps {
                sh '''
                    ls -la 
                    node --version
                    npm --version
                '''
            }
        }
    }
}