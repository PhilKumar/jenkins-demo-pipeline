pipeline {
  agent any

  parameters {
    choice(name: 'ENV', choices: ['dev', 'staging', 'prod'], description: 'Choose environment')
    string(name: 'APP_VERSION', defaultValue: '1.0.0', description: 'App version to deploy')
  }

  stages {
    stage('Build') {
      steps {
        echo "Building version: ${params.APP_VERSION} for ${params.ENV}"
      }
    }
  }

stage('Approval') {
  steps {
    input message: 'Do you want to deploy to production?', ok: 'Deploy Now'
  }
}

  stage('Deploy') {
    when {
      expression { params.ENV == 'prod' }
    }
    steps {
      echo "Deploying version: ${params.APP_VERSION} to production"
    }
  }
}