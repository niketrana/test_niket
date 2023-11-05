

pipeline {
    agent any
        env {
    //DOCKER_REGISTRY = 'your-docker-registry'
    IMAGE_NAME = 'niket-image'
    BRANCH_NAME = 'main'
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
                // Build a Docker image from the Dockerfile in the repository
                script {
                    docker.image("${env.IMAGE_NAME}:${env.BRANCH_NAME}").build()
                }
            }
        }
    }
}
