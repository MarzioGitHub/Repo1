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
  post {
        always {
            emailext body: 'Test email inviata dalla Pipeline di Marzio', recipientProviders: 'armando.calabro@atos.net', subject: 'JenkinsPipelineTest'
        }
}
