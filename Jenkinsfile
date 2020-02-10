pipeline {
  agent any
  stages {
    stage('error') {
      agent {
        docker {
          image 'maven:3-alpine'
          args '-v /root/.m2:/root/.m2'
        }

      }
      steps {
        sh 'npm install'
      }
    }

  }
}