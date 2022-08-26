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
          steps {
            sh 'echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"'
          }
        }

        stage('Maven Building 3') {
          steps {
            sh 'echo \'Maven Building 3 ....\''
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo \'Testing....\''
          }
        }

        stage('') {
          steps {
            sh 'sh \'node --version\''
          }
        }

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