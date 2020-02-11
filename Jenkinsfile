pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          image 'maven:3-alpine'
          args '-v /root/.m2:/root/.m2'
        }

      }
      steps {
        sh '''sh \'mvn clean install\'
def pom = readMavenPom file:\'pom.xml\'
            print pom.version
            env.version = pom.version'''
      }
    }

  }
}