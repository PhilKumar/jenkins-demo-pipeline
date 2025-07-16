pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/PhilKumar/jenkins-demo-pipeline.git'
      }
    }

    stage('Build') {
      steps {
        echo 'Running build...'
      }
    }

    stage('Test') {
      steps {
        echo 'Running unit tests...'
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
