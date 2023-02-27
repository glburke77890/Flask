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
        stage('AWS Commands'){
            steps{
                script{
                    withAWS(credentials: 'AWS', region: 'us-east-1'){
                        sh 'aws sts get-caller-identity'
                    }
                }
            }
        }
    }
}