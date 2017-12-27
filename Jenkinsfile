pipeline {
  agent any
  stages {
    stage('Build and Release') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('test') {
      steps {
        parallel(
          "test": {
            echo 'testing'
            
          },
          "code quality analysis": {
            echo 'code'
            
          }
        )
      }
    }
    stage('deploy in dev') {
      steps {
        echo 'depoy in dev'
      }
    }
  }
}