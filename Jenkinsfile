/*
============================================================
Jenkins CI/CD Pipeline for Go Web Application
============================================================

Pipeline Workflow

1. Clone the source code from GitHub
2. Run Go unit tests
3. Build Docker image
4. Deploy application container

This demonstrates a simple CI/CD pipeline using Jenkins
and Docker.

============================================================
*/

pipeline {

    agent {
        label {
            label 'master'
            customWorkspace "${JENKINS_HOME}/${BUILD_NUMBER}/"
        }
    }

    environment {

        /*
        Enable Go modules
        This allows dependency management
        */
        GO111MODULE = 'on'
    }

    stages {

        stage('Clone Repository') {

            /*
            Pull source code from GitHub
            */

            steps {
                git 'https://github.com/kodekloudhub/go-webapp-sample.git'
            }
        }


        stage('Run Tests') {

            /*
            Run all Go unit tests
            */

            steps {
                sh 'go test ./...'
            }
        }


        stage('Build Docker Image') {

            /*
            Build Docker image from Dockerfile
            */

            steps {

                script {
                    image = docker.build("adminturneddevops/go-webapp-sample")
                }

            }
        }


        stage('Deploy Application') {

            /*
            Run container and expose application

            Host Port: 8090
            Container Port: 8000
            */

            steps {

                sh "docker run -p 8090:8000 -d adminturneddevops/go-webapp-sample"

            }

        }

    }

}
