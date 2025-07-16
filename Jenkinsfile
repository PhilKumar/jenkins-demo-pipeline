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
}