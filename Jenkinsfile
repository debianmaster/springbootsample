pipeline {
  agent {
    docker {
      image 'gradle'
    }
    
  }
  stages {
    stage('Build') {
      agent {
        docker {
          image 'maven'
        }
        
      }
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
  environment {
    name = 'dev'
  }
}