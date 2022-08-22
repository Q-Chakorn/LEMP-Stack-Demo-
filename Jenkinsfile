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
    }

        stage('Build docker image') {
            steps {
                script {
                    sh "cd php/"
                    sh "ll"
                    docker.withRegistry('', 'dockerhub') {
                    //sh "docker build -t chakorn/php"
                        //def slackImage = docker.build("${env.image}:${BUILD_NUMBER}")
                        //slackImage.push()
                        //slackImage.push('latest')
                    }
                }
            }
        }
        //stage('Deployment'){
            //steps {
                //sh "docker-compose up -d"
            //}
            
        //}
}