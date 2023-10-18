pipeline {
  agent any
  stages {
    stage('Docker Build ') {
      steps {
        sh 'docker build -t abdelkefiismail/book-saw:latest .'
      }
    }

    stage('Docker Push') {
      steps {
        sh '''docker tag abdelkefiismail/book-saw:latest abdelkefiismail/book-saw:latest
'''
        sh 'docker push abdelkefiismail/book-saw:latest'
      }
    }

  }
}