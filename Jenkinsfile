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
                sh "docker run hello-world &"
            }
        }
    }   
}
