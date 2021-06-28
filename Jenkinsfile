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
                sh "echo 'test check pull request'"
                sh "docker run hello-world &"
            }
        }
    }   
}
