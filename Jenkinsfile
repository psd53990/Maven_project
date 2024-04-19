pipeline {
    agent any

    stages {
        stage('Cleaning stage') {
            steps {
                bat 'mvn clean'
            }
        }
        
        stage('Testing stage') {
            steps {
                bat 'mvn test'
            }
        }
        
        stage('Packaging stage') {
            steps {
                bat 'mvn package'
            }
        }
    }
    
    post {
        always {
            echo 'This will always run regardless of the result.'
        }
        success {
            echo 'Build was successful!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
