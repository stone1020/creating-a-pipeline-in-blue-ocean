pipeline {
  agent {
    docker {
      image 'node:7-alpine'
    }

  }
  stages {
    stage('Maven Build') {
      parallel {
        stage('Maven Build') {
          agent any
          steps {
            sh 'echo \'Maven Building....\''
            echo 'Maven Build'
          }
        }

        stage('Maven Build 2') {
          agent any
          steps {
            sh 'echo "Running..."'
          }
        }

        stage('Maven Building 3') {
          agent any
          steps {
            sh 'echo \'Maven Building 3 ....\''
          }
        }

      }
    }

    stage('Test') {
      agent any
      steps {
        sh 'echo \'Testing....\''
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