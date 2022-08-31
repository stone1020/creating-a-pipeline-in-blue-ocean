pipeline {
  agent none
  stages {
    stage('Build') {
      parallel {
        stage('node') {
          agent {
            docker {
              image 'node:7-alpine'
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
      agent none
      steps {
        sh 'echo \'Delivering....\''
      }
    }

    stage('Sonar Check') {
      agent none
      steps {
        sh 'echo \'Sonar Checking....\''
      }
    }

    stage('Docker Build') {
      agent none
      steps {
        sh 'echo \'Docker Building....\''
      }
    }

    stage('Rancher Deploy') {
      agent none
      steps {
        sh 'echo \'Rancher Deploying....\''
      }
    }

  }
  environment {
    DB_ENGINE = 'MySQL'
  }
}
