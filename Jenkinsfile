pipeline {
  agent {
    docker {
      image 'gradle'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        echo 'Build'
        sh 'gradle clean build'
      }
    }
    stage('Test') {
      steps {
        sh '''grade bootrun
ls -lrt'''
      }
    }
  }
}