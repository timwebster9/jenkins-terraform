pipeline {
  agent {
    label 'caf'
  }
  stages {
    stage('Hello') {
      environment {
        SERVICE_CREDS = credentials('azure-jenkins-launchpad-sp')
      }
      steps {
        sh 'terraform init'
        sh 'terraform plan'
      }
    }
  }
}
