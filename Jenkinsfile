pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            bat(script: 'echo hello', encoding: 'utf-8', returnStdout: true, returnStatus: true)
            sleep 5
          }
        }

        stage('andirod') {
          steps {
            echo 'andrid'
          }
        }

      }
    }

    stage('scan') {
      parallel {
        stage('scan') {
          steps {
            echo 'world'
          }
        }

        stage('error') {
          steps {
            echo 'sonar'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'test'
      }
    }

  }
}