pipeline {
  agent {
    label 'caf'
  }
  stages {
    stage('Hello') {
      environment {
        SERVICE_CREDS = credentials('AV_LAUNCHPAD_SP')
      }
      steps {
        sh 'terraform init'
        sh 'terraform plan'
      }
    }
  }
}
