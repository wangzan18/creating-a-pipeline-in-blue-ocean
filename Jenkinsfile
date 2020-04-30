pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 4000:3000'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'npm install'
      }
    }

    stage('test') {
      agent {
        docker {
          image 'nginx'
        }

      }
      steps {
        sleep 60
      }
    }

  }
}