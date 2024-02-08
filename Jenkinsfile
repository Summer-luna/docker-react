pipeline {
    agent any
    stages {
        stage('build') {
            agent {
              label "docker-agent-alpine"
            }
            steps {
                sh """
                  docker build -t react-docker .
                """
            }
        }
        stage('run') {
          agent {
              label "docker-agent-alpine"
            }
          steps {
                sh """
                  docker run --rm react-docker
                """
            }
        }
    }
}
