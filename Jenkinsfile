pipeline {
  agent any
  stages {
    stage('bulild') {
      parallel {
        stage('bulild') {
          steps {
            junit(testResults: '*.xml', allowEmptyResults: true)
            build(propagate: true, job: '1')
            sh 'echo adnan'
          }
        }

        stage('test') {
          steps {
            sh 'echo test'
            echo 'hello'
          }
        }

      }
    }

    stage('sleep') {
      parallel {
        stage('sleep') {
          steps {
            sleep 33
          }
        }

        stage('sleep2') {
          steps {
            sleep 3
          }
        }

      }
    }

    stage('test') {
      steps {
        fileExists '.xml'
        git(url: 'dsdfa.com', branch: 'sdsfd', changelog: true, poll: true, credentialsId: 'adnan')
      }
    }

  }
  environment {
    name = 'adnan'
    docker_vers = '1.8'
  }
}