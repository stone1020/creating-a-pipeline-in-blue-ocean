pipeline {
  agent none
  stages {
    stage('node') {
      agent {
        docker {
          image 'node:7-alpine'
        }

      }
      steps {
        echo 'Node Build'
      }
    }

    stage('maven-test') {
      steps {
        sh 'sh \'mvn --version\''
      }
    }

    stage('Deliver') {
      steps {
        sh 'echo \'Delivering....\''
      }
    }

    stage('Sonar Check') {
      steps {
        sh 'echo \'Sonar Checking....\''
      }
    }

    stage('Docker Build') {
      steps {
        sh 'echo \'Docker Building....\''
      }
    }

    stage('Rancher Deploy') {
      steps {
        sh 'echo \'Rancher Deploying....\''
      }
    }

  }
}