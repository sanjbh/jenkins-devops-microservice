pipeline{
    //agent any
    agent {
        docker {
            image 'maven:3.6.3'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
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


