
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Task: Build the code using a build automation tool updated.'
                    echo 'Tool: Maven'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Task: Run unit tests to ensure code functions as expected and integration tests.'
                    echo 'Tool: JUnit'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Unit and Integration Tests Status: ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Task: Analyze the code to ensure it meets industry standards.'
                    echo 'Tool: SonarQube'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Code Analysis Status: ${currentBuild.currentResult}",
                        body: "The Code Analysis stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                script {
                    echo 'Task: Perform a security scan on the code to identify vulnerabilities.'
                    echo 'Tool: OWASP Dependency-Check'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Security Scan Status: ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Task: Deploy the application to a staging server.'
                    echo 'Tool: Custom deployment script'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Deploy to Staging Status: ${currentBuild.currentResult}",
                        body: "The Deploy to Staging stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Task: Run integration tests on the staging environment to ensure functionality.'
                    echo 'Tool: Maven or similar'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Integration Tests on Staging Status: ${currentBuild.currentResult}",
                        body: "The Integration Tests on Staging stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Task: Deploy the application to a production server.'
                    echo 'Tool: Custom deployment script'
                }
            }
            post {
                always {
                    mail to: 'hashinigunathilake7@gmail.com',
                        subject: "Deploy to Production Status: ${currentBuild.currentResult}",
                        body: "The Deploy to Production stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
    }
}
