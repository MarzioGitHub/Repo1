pipeline {
  agent any
  stages {
    stage('FirstStage') {
      agent any
      steps {
        echo '"Start Pipeline"'
        sh 'echo PATH = ${PATH}'
        mail(subject: 'JenkinsPipeline', body: 'Mail scritta da uno step della pipeline di Marzio.', from: 'marzio.sottotetti@gmail.com', to: 'armando.calabro@atos.net')
        echo 'Mail Inviata'
      }
    }
  }
}