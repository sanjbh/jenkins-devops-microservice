pipeline{
    environment {
        JAVA_TOOL_OPTIONS = '-Duser.home=/root'
    }
    // agent any
    // agent {
    //     docker {
    //         image 'node:current-alpine3.16'
    //     }
    // }
    agent {
        docker {
            image 'maven:3-jdk-8-alpine'
            args '-v /var/jenkins_home:/root'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile deploy'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Integration Test') {
            steps {
                sh 'mvn failsafe:integration-test failsafe:verify'
            }
        }
    } 
    post {
        always {
            echo "I am done with the pipeline"
        }
    }
}


