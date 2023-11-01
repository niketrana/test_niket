pipeline {
    agent none
    stages {
        //DEV
        stage('stage1') {
            agent {
              label {
                label 'stage1a'
                }
            }
            steps {
                echo stage1
            }
        }
        stage('stage2') {
            agent {
              label {
                label 'stage2b'
                }
            }
            steps {
                echo stage2
            }
        }
    } // Stages
} // Pipeline
