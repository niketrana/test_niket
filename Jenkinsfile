pipeline {
    agent any
    stages {
        stage('hw') {
            steps {
               echo "hw"
            }            
        }    
        stage('GitClone') {
            steps {
               sh 'git clone https://github.com/niketrana/test_niket2.git'
            }            
        }    
        stage('Build Image') {
            steps {
                 docker build -t niket-image:v1.0 Dockerfile
                   }            
        }
    }
}    // test
