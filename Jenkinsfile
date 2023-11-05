pipeline {
    agent any

    environment {
        // DOCKER_REGISTRY = 'your-docker-registry'
        IMAGE_NAME = 'niket-image'
        IMAGE_TAG = 'v:1.0'
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
                    sh "docker build -t ${IMAGE_NAME}:${IMAGE_TAG} ."
                }
            }
        }
    }
}
