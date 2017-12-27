pipeline {
  agent {
    docker {
      image 'docker:dind'
    }
    
  }
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