pipeline {
  agent none
  stages {
    stage('build') {
      steps {
        sh '''pwd   
              date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Hello Test'
            echo 'parallel testing'
          }
        }

        stage('Test2') {
          steps {
            echo 'Hello2'
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            sleep 13
          }
        }

        stage('Dev-Develop') {
          steps {
            sh 'java -version'
          }
        }

      }
    }

  }
}
