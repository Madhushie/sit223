pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Using Maven for Build'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Using JUnit for Tests'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Using SonarQube for Code Analysis'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Using OWASP ZAP for Security Scan'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Using AWS CLI to Deploy to Staging'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Using Selenium for Integration Tests'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Using AWS CLI to Deploy to Production'
            }
        }
    }

    post {
        success {
            emailext subject: 'Pipeline Status: Success', body: 'The Jenkins pipeline has completed successfully.', to: 'madhushihidellarachchi@gmail.com'
        }
        failure {
            emailext subject: 'Pipeline Status: Failure', body: 'The Jenkins pipeline has failed.', to: 'madhushihidellarachchi@gmail.com'
        }
    }
}
