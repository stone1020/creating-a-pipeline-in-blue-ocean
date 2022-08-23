pipeline {
  agent any
  stages {
    stage('Maven Build') {
      steps {
        sh 'echo \'Maven Building....\''
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