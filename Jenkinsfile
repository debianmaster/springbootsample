pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
        git(url: 'https://github.com/debianmaster/springbootsample', branch: 'master', changelog: true, poll: true)
      }
    }
  }
}