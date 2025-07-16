pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Running build...'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests...'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying application...'
      }
    }
  }

  post {
    success {
      echo '✅ Pipeline succeeded!'
    }
    failure {
      echo '❌ Pipeline failed!'
    }
  }
}
