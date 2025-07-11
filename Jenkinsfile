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

        stage('') {
          steps {
            echo 'hello'
          }
        }

      }
    }

    stage('') {
      steps {
        sleep 3
      }
    }

    stage('final') {
      steps {
        sh '''touch a.txt
ls
echo "hello world"'''
      }
    }

  }
}