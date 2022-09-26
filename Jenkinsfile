pipeline{
    //agent any
    agent {
        docker {
            image 'node:current-alpine3.16'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'node --version'
                sh 'pwd'
                sh 'ls -ltr'
                sh 'cat /etc/os-release'
                echo "Build"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test"
            }
        }
    } 
    post {
        always {
            echo "I am done with the pipeline"
        }
    }
}


