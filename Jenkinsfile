pipeline {
    agent {
        docker {
            image 'node:18-alpine'
        }
    }

    stages {
        stage('Hello') {
            steps {
                sh 'node -v'
            }
        }
    }
}
