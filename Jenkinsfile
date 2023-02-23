pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t glburke77890/flaskapp .'
            }
        }
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