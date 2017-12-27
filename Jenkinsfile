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
        sh 'ls -lrt'
      }
    }
  }
}