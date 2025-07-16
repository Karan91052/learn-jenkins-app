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
                    cleanWs()
                    ls -la 
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}