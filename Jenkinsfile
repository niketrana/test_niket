env {
    //DOCKER_REGISTRY = 'your-docker-registry'
    IMAGE_NAME = 'niket-image'
    BRANCH_NAME = 'main'
}

pipeline {
    agent any

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
                    def customImage = docker.build("${env.IMAGE_NAME}:${env.BRANCH_NAME}")
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                // Push the Docker image to the specified container registry
                script {
                    customImage.push()
                }
            }
        }
    }

    post {
        success {
            // This block is executed when the pipeline is successful
            echo "Pipeline successful for branch ${env.BRANCH_NAME}"
        }

        failure {
            // This block is executed when the pipeline fails
            mail to: 'youremail@example.com', subject: "Pipeline Failed: ${currentBuild.fullDisplayName}", body: "The pipeline has failed for branch ${env.BRANCH_NAME}."
        }
    }
}
