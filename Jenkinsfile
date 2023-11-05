pipeline {
    agent any
    stages {
        stage('hello-world') {
            steps {
               echo "Hello World !!!!!!!!!!!!!!!!!!!!!!!!!!!!!"
            }            
        }    
        stage('GitClone') {
            steps {
               sh 'git clone https://github.com/niketrana/test_niket2.git'
            }            
        }    
        stage('Build Image') {
            steps {
                 sh "docker build -t niket-image:v1.0 ."
                   }            
        }
    }
}    // test
