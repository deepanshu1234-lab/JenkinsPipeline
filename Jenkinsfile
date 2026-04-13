pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Task: Compile and package the source code into a deployable artifact.'
                echo 'Tool: Maven - used to compile Java code and package it into a JAR/WAR file.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Run unit tests to verify individual functions work correctly.'
                echo 'Task: Run integration tests to verify all components work together.'
                echo 'Tool: JUnit for unit testing, TestNG for integration testing.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Analyse source code for bugs, code smells, and coding standard violations.'
                echo 'Tool: SonarQube - integrates with Jenkins to provide detailed code quality reports.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scan code and dependencies for known security vulnerabilities (CVEs).'
                echo 'Tool: OWASP Dependency-Check - identifies vulnerable libraries in the project.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Task: Deploy the packaged application to a staging server for pre-production testing.'
                echo 'Tool: AWS CodeDeploy - automates deployment to an AWS EC2 staging instance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Run integration tests on staging to ensure app works in production-like environment.'
                echo 'Tool: Selenium - automates browser-based integration testing against the staging server.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Task: Deploy the verified application to the live production server.'
                echo 'Tool: AWS CodeDeploy - deploys to production AWS EC2 instance after all checks pass.'
            }
        }

    }
}
