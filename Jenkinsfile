pipeline {
    agent { label "docker-agent-alpine" }
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
                  docker run --rm react-docker
                """
            }
        }
    }
}
