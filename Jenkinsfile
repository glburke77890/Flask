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
                    withDockerRegistry(credentialsId; 'Docker'){
                        docker push glburke77890/flaskapp
                    }
                }
            }
        }
    }
}