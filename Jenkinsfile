pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'ls'
          }
        }

        stage('error') {
          steps {
            echo 'hello'
          }
        }

      }
    }

    stage('error') {
      steps {
        sleep 3
      }
    }

    stage('final') {
      steps {
        slackSend(channel: 'new-channel', message: 'hi')
        sh '''touch a.txt
ls
echo "hello world"'''
      }
    }

  }
}