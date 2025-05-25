pipeline {
    agent any
    tools {
        maven 'Maven-3.8.6' // This specifies which Maven tool version to use
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/user/maven-project.git' // Check out the repository
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package' // Run the Maven build command on Windows (use 'sh' for Linux/macOS)
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test' // Run the Maven test command (use 'sh' for Linux/macOS)
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...' // Simulate deployment (you can replace it with actual deploy steps)
            }
        }
    }
    post {
        success {
            echo 'Build and Test Passed! 🎉' // This message will be shown if the build and test pass
        }
        failure {
            echo 'Build Failed! 🚨' // This message will be shown if the build or test fails
        }
    }
}
