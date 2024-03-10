pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Compile the hello.cpp file located inside the main directory
                sh 'g++ -o main/hello main/hello.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                // Execute the compiled hello.cpp file
                sh './main/hello'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps if needed
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
