pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                build "PES2UG22CS212_1"
                sh 'g++ main/hello.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
