pipeline {
    agent any

    environment {
        DIRECTORY_PATH = 'SIT753-Jenkins-Pipeline'
        TESTING_ENVIRONMENT = 'Staging Server'
        PRODUCTION_ENVIRONMENT = 'Avinash Production Environment'
    }

    stages {
        stage('Build') {
            steps {
                echo "Build Tool: Maven"
                echo "Fetch the source code from the directory path specified by the environment variable: ${DIRECTORY_PATH}"
                echo "Compile and package the code using Maven"
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo "Testing Tools: JUnit and Selenium"
                echo "Run unit tests to check individual function"
                echo "Run integration tests to check connected components"
            }
        }

        stage('Code Analysis') {
            steps {
                echo "Code Analysis Tool: SonarQube"
                echo "Analyse the code quality and check whether it follows coding standards"
            }
        }

        stage('Security Scan') {
            steps {
                echo "Security Tool: OWASP Dependency-Check"
                echo "Scan the project dependencies to identify known vulnerabilities"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deployment Tool: AWS EC2"
                echo "Deploy the application to the staging environment: ${TESTING_ENVIRONMENT}"
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo "Testing Tool: Postman/Newman"
                echo "Run integration tests on the staging environment"
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deployment Tool: AWS EC2"
                echo "Deploy the application to the production environment: ${PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
