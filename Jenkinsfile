pipeline {
    agent any

    environment {
        EMAIL = 'hashinigunathilake7@gmail.com'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Task - Build the code using a build automation tool'
                    echo 'Tool - Maven'
                }
            }
             post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Unit and Integration Tests - ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
        }

        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Task - Run unit tests to ensure the code functions'
                    echo 'Tool - JUnit'
                }
            }
            post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Unit and Integration Tests - ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
            }
        }

        stage('Code Analysis') {
            steps {
                script {
                    echo 'Task - Integrate a code analysis tool'
                    echo 'Tool - SonarQube'
                }
            }
             post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Unit and Integration Tests - ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
        }

        stage('Security Scan') {
            steps {
                script {
                    echo 'Task - Perform a security scan on the code using a tool to identify any vulnerabilities'
                    echo 'Tool - OWASP Dependency-Check'
                }
            }
            post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Security Scan - ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Task - Deploy the application to a staging server'
                    echo 'Tool - AWS EC2'
                }
            }
             post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Security Scan - ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
            }
        }

        stage('Integration Test on Staging') {
            steps {
                script {
                    echo 'Task - Run integration tests on the staging environment to ensure the application'
                    echo 'Tool - Maven'
                }
            }
             post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Security Scan - ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Task - Deploy the application to a production server'
                    echo 'Tool - AWS EC2'
                }
            }
             post {
                always {
                    emailext(
                        to: "${env.EMAIL}",
                        subject: "Security Scan - ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true
                    )
                }
            }
        }
    }
}
