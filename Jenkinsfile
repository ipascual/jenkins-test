pipeline {
  agent any
  parameters {
    string(name: 'BRANCH',
           description: 'What branch to deploy?')
    string(name: 'PACKAGE_NAME',
           description: 'What package name do you want?')
  } 
  stages {
    stage('Build') {
      steps {
        build 'Build', parameters: [
          string(name: 'BRANCH', value: String.valueOf(BRANCH))
        ]
      }
    }
    stage('Package') {
      steps {
        build 'Package'
      }
    }
  }
}
