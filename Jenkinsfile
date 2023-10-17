pipeline {
  agent {
    node {
      label 'main'
    }

  }
  stages {
    stage('Docker Build') {
      agent {
        node {
          label 'main'
        }

      }
      steps {
        sh 'docker build -t abdelkefiismail/book-saw:latest .'
      }
    }

    stage('Docker Push') {
      agent {
        node {
          label 'main'
        }

      }
      steps {
        sh 'docker tag abdelkefiismail/book-saw:latest abdelkefiismail/book-saw:latest'
        sh 'docker push abdelkefiismail/book-saw:latest'
      }
    }

  }
}