pipeline {
    agent any

    environment {
        // DOCKER_REGISTRY = 'your-docker-registry'
        IMAGE_NAME = 'niket-image'
        IMAGE_TAG = 'v1.0'
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
                    // Define the Docker image
                    def dockerImage = docker.build("${env.IMAGE_NAME}:${env.IMAGE_TAG}")

                    // Build the Docker image from the Dockerfile in the repository
                    dockerImage.build()
                }
            }
        }
    }
}
