pipeline {
    agent any

    stages {
        stage('Login and Push'){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'Docker'){
                        docker.build('glburke77890/flaskapp').push('latest')
                    }
                }
            }
        }
    }
}