pipeline{
    agent any

    environment {
        image = "chakorn/nodejs"
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
}