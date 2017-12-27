pipeline {
  agent any
  stages {
    stage('Build') {
      agent {
        docker {
          image 'gradle'
        }
        
      }
      steps {
        echo 'Build'
        sh 'gradle clean build'
      }
    }
    stage('Test') {
      agent {
        node {
          label 'gradle'
        }
        
      }
      steps {
        sh '''grade bootrun
ls -lrt'''
      }
    }
  }
  environment {
    name = 'dev'
  }
}