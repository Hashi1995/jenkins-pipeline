pipeline {
    agent any

    environment {
        EMAIL_RECIPIENT = 'hashinigunathilake7@gmail.com'
    }

    stages {
        stage('build') {
            steps {
                script {
                    echo 'Task - Build the code using a build automation tool'
                    echo 'Tool - Maven'
                }
            }
            post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('unit and Integration Tests') {
            steps {
                script {
                    echo 'Task - Run unit tests to ensure the code functions'
                    echo 'Tool - JUnit'
                }
            }
            post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('code Analysis') {
            steps {
                script {
                    echo 'Task - Integrate a code analysis tool'
                    echo 'Tool - SonarQube'
                }
            }
            post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('security Scan') {
            steps {
                script {
                    echo 'Task - Perform a security scan on the code using a tool to identify any vulnerabilities'
                    echo 'Tool - OWASP Dependency-Check'
                }
            }
           post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('deploy to Staging') {
            steps {
                script {
                    echo 'Task - Deploy the application to a staging server'
                    echo 'Tool - AWS EC2'
                }
            }
            post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('integration Test on Staging') {
            steps {
                script {
                    echo 'Task - Run integration tests on the staging environment to ensure the application'
                    echo 'Tool - Maven'
                }
            }
            post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('deploy to Production') {
            steps {
                script {
                    echo 'Task - Deploy the application to a production server'
                    echo 'Tool - AWS EC2'
                }
            }
            post {
                always {
                    mail to: "${env.EMAIL_RECIPIENT}",
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
    }
}
