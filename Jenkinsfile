pipeline {
  agent none
  stages {
    stage('Build') {
      parallel {
        stage('node') {
          agent {
            docker {
              image 'node:7-alpine'
              args '-p 3000:3000'
            }

          }
          steps {
            sh 'node --version'
          }
        }

        stage('maven') {
          agent {
            docker {
              image 'maven:3-alpine'
            }

          }
          steps {
            sh 'printenv'
          }
        }

      }
    }

    stage('Deliver') {
      agent any
      steps {
        sh 'echo \'Delivering....\''
      }
    }

    stage('Sonar Check') {
      agent any
      steps {
        sh 'echo \'Sonar Checking....\''
      }
    }

    stage('Docker Build') {
      agent any
      steps {
        sh 'echo \'Docker Building....\''
      }
    }

    stage('Rancher Deploy') {
      agent any
      steps {
        sh 'echo \'Rancher Deploying....\''
      }
    }

  }
  environment {
    DB_ENGINE = 'MySQL'
  }
}