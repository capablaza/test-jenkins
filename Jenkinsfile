pipeline {
    agent any

    stages {
        stage('Checkout'){
            steps{
                checkout scm
            }            
        }   
        stage('Clean images not used'){
            steps{
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    sh "docker images -a --no-trunc | grep 'none' | awk '{print \$3}' | xargs docker rmi"
                    sh "docker rmi -f ${IMAGE_NAME}"
                }                 
            }            
        }             
        stage('Run Container'){
            steps {
                sh "docker run hello-world &"
            }
        }
    }   
}
