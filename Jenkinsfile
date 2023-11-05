pipeline {
    agent any

    environment {
//        DOCKER_REGISTRY = 'your-docker-registry'
        IMAGE_NAME = 'your-image-name'
        IMAGE_TAG = 'latest'
    }

    stages {
        stage('Checkout') {
            steps {
                // Check out the code from the Git repository
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Build a Docker image from the Dockerfile in the repository
                    sh "docker build -t {IMAGE_NAME}:${IMAGE_TAG} ."
                }
            }
        }
    }
    }
