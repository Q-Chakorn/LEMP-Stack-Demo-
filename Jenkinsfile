pipeline{
    agent any

    environment {
        image = "chakorn/php"
        registry = "docker.io"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Print Environment') {
            steps {
                sh('ls -al')
                sh('printenv')
            }
        }
        stage('Build docker image') {
            steps {
                script {
                    docker.withRegistry('', 'dockerhub') {
                    //sh "ls -a"
                    //sh "docker build -t chakorn/php -f php/Dockerfile ."
                    //sh "docker push chakorn/php:latest"
                        //def slackImage = docker.build("${env.image}:${BUILD_NUMBER}")
                        //slackImage.push()
                        //slackImage.push('latest')
                    }
                }
            }
        }
        stage('Deployment'){
            steps {
                sh "docker-compose up -d"
            }
        }
    }
}
