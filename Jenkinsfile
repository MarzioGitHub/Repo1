pipeline {
  agent any
  stages {
    stage('FirstStage') {
      agent any
      steps {
        echo '"Start Pipeline"'
        sh 'echo PATH = ${PATH}'
      }
    }
  }
}