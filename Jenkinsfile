pipeline {
    agent {
      label 'agent1'
    }
    stages {
       stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
      }
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
