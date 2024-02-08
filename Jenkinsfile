pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh """
                  docker build -t react-docker .
                """
            }
        }
        stage('run') {
          steps {
                sh """
                  docker run --rm -d -p 3000:80 react-docker
                """
            }
        }
    }
}
