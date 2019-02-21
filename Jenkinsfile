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
        build job: 'Develop/Build', parameters: [string(name: 'BRANCH', value: String.valueOf(BRANCH))]
      }
    }
    stage('Package') {
      steps {
        build job: 'Develop/Package', parameters: [string(name: 'PACKAGE_NAME', value: String.valueOf(PACKAGE_NAME))]
      }
    }
  }
}
