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
    stage('SecondStage') {
      agent any
      steps {
        fileExists 'TestFile1.sh'
      }
    }
    stage('NotExist') {
      parallel {
        stage('NotExist') {
          agent any
          steps {
            writeFile(file: 'TestWrite.txt', text: 'File creato dalla Pipeline.')
          }
        }
        stage('Exist') {
          agent any
          steps {
            sh '''#!/bin/sh
echo START ESECUZIONE SCRIPT;'''
          }
        }
      }
    }
  }
}