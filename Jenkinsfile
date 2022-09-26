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
            image 'maven:3.8.1-openjdk-17-slim'
            args '-v /var/jenkins_home:/root'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "$PATH"
                echo "Build number: $env.BUILD_NUMBER"
                echo "Build id: $env.ID"
                echo "Job name: $env.JOB_NAME"
                echo "Build tag: $env.BUILD_TAG"
                sh 'pwd'
                sh 'ls -ltra /root'
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


