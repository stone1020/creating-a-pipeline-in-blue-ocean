pipeline {
  agent any
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
            sh 'echo \'Maven Building 2 ....\''
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