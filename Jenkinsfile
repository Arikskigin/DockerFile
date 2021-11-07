pipeline {
   
    stages {
        stage('Build') {
            steps {
               sh " docker build -t Dockerfile "
            }
        }
        stage('run') {
            steps {
                 sh " docker run -rm Dockerfile "
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo " deploying with ${SERVER_CRED}"
                sh "${SERVER_CRED}"
            }
        }
    }
}
