pipeline {
  agent {
    label 'caf'
  }
  stages {
    stage('Hello') {
      environment {
        ARM_CLIENT_ID = credentials('av-launchpad-sp-app-id')
        ARM_CLIENT_SECRET = credentials('av-launchpad-sp-secret')
        ARM_SUBSCRIPTION_ID = credentials('av-caf-bootstrap-sub-id')
        ARM_TENANT_ID = credentials('av-tenant-id')
      }
      steps {
        sh 'terraform init'
        sh 'terraform plan'
      }
    }
  }
}
