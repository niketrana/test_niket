pipeline {
    agent any
    stages {
        stage('HelloWorld') {
            steps {
               echo "Hello World"
            }
        stage('GitClone') {
            steps {
               git "https://github.com/niketrana/test_niket2.git"
            }            
        }
    }
}    
