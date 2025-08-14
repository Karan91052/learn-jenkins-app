pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
               sh '''
                    curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
                    sudo apt-get install -y nodejs
                    node -v
                    npm -v
                      '''
            }
        }

        stage('Test') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                echo 'Running Test Stage - placeholder for test execution'
            }
        }
    }
}
