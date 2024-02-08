pipeline {
    agent any
    stages {
        stage('build') {
            environment {
                HOME = "${env.WORKSPACE}"
            }
            steps {
                sh """
                  sudo docker build -t react-docker .
                """
            }
        }
        stage('run') {
          steps {
                sh """
                  sudo docker run --rm -d -p 3000:80 react-docker
                """
            }
        }
    }
}
