pipeline {
  agent any
  stages {
    stage('Code Pull') {
      agent any
      steps {
        dir(path: '/opt/')
        git(url: 'https://github.com/AKI-25/AKI-25.github.io.git', branch: 'master')
      }
    }

    stage('Docker Build') {
      steps {
        sh 'docker build -t abdelkefiismail/book-saw:latest .'
      }
    }

    stage('Docker Push') {
      steps {
        sh 'docker tag abdelkefiismail/book-saw:latest abdelkefiismail/book-saw:latest'
        sh 'docker push abdelkefiismail/book-saw:latest'
      }
    }

  }
}