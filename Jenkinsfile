pipeline {
    agent any

    stages {
        stage('Checkout'){
            steps{
                checkout scm
            }            
        }                    
        stage('Run Container'){
            steps {
                sh "echo 'test 2'"
                sh "docker run hello-world &"
            }
        }
    }   
}
