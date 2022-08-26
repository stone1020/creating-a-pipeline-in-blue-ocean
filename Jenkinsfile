pipeline {
  agent none
  stages {
    stage('Maven') {
      agent {
        docker {
          image 'maven:3.3.3'
        }

      }
      steps {
        sh 'mvn --version'
        echo 'Maven Build'
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