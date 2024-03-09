pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "building"'
                build 'PES1UG21CS081-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "testing"'
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "deploying"' 
                sh 'echo "deployed"'
            }
        }
    }
    post{
        failure{
            error 'pipeline failed'
        }
    }
}
