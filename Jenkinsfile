pipeline {
  agent none
  stages {
    stage('Maven Build') {
      parallel {
        stage('Maven') {
          agent {
            docker {
              image 'maven:3.3.3'
            }

          }
          steps {
            sh 'sh \'mvn --version\''
            echo 'Maven Build'
          }
        }

        stage('Python') {
          agent {
            docker {
              image 'python:3.5.1'
            }

          }
          steps {
            sh 'sh \'python --version\''
          }
        }

        stage('Node') {
          agent {
            docker {
              image 'node:6.3'
            }

          }
          steps {
            sh 'sh \'npm --version\''
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('maven-test') {
          steps {
            sh 'sh \'mvn --version\''
          }
        }

        stage('python-test') {
          steps {
            sh 'sh \'python --version\''
          }
        }

        stage('node-test') {
          steps {
            sh 'sh \'npm --version\''
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