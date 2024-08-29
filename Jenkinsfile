pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Task: Build the code using a build automation tool.'
                    echo 'Tool: Maven'
                    // Example Maven build command
                    // sh 'mvn clean package'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Task: Run unit tests to ensure code functions as expected and integration tests.'
                    echo 'Tool: JUnit'
                    // Example JUnit test command
                    // sh 'mvn test'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Unit and Integration Tests Status: ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Task: Analyze the code to ensure it meets industry standards.'
                    echo 'Tool: SonarQube'
                    // Example SonarQube command
                    // sh 'sonar-scanner'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Code Analysis Status: ${currentBuild.currentResult}",
                        body: "The Code Analysis stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                script {
                    echo 'Task: Perform a security scan on the code to identify vulnerabilities.'
                    echo 'Tool: OWASP Dependency-Check'
                    // Example security scan command
                    // sh 'dependency-check.sh'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Security Scan Status: ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Task: Deploy the application to a staging server.'
                    echo 'Tool: Custom deployment script'
                    // Example deployment command
                    // sh 'deploy-to-staging.sh'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Deploy to Staging Status: ${currentBuild.currentResult}",
                        body: "The Deploy to Staging stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Task: Run integration tests on the staging environment to ensure functionality.'
                    echo 'Tool: Maven or similar'
                    // Example integration test command
                    // sh 'mvn verify'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Integration Tests on Staging Status: ${currentBuild.currentResult}",
                        body: "The Integration Tests on Staging stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Task: Deploy the application to a production server.'
                    echo 'Tool: Custom deployment script'
                    // Example production deployment command
                    // sh 'deploy-to-production.sh'
                }
            }
            post {
                always {
                    emailext (
                        subject: "Deploy to Production Status: ${currentBuild.currentResult}",
                        body: "The Deploy to Production stage has completed with status: ${currentBuild.currentResult}.",
                        to: 'hashinigunathilake7@gmail.com'
                    )
                }
            }
        }
    }
}
