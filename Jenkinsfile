pipeline {
    agent any

    environment{
        DOCKER = credentials('Docker')
    }

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t glburke77890/flaskapp .'
            }
        }
        stage('Login'){
            steps{
                echo '$DOCKER | docker login -u glburke77890 --password-stdin'
            }
        }
        stage('Push'){
            steps{
                sh 'docker push glburke77890/flask'
            }

        }
    }
}