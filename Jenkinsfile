pipeline {
  agent any

  environment {
    GIT_CRED_ID = 'SVC-JENKINS-ADM'

  }

  stages {
    stage('Trigger based on branch changes') {
      when {
        expression { return env.BRANCH_NAME == 'a' || env.BRANCH_NAME == 'b' || env.BRANCH_NAME == 'c' }
      }
      steps {
        script {
          echo "Changes detected in branch ${env.BRANCH_NAME}"
          echo "Current user is ${env.GIT_CRED_ID}"
          
          
        if (env.BRANCH_NAME == 'a') {
          echo "Changes in branch a"
        } else if (env.BRANCH_NAME == 'b') {
          echo "Changes in branch b"
        } else if (env.BRANCH_NAME == 'c') {
          echo "Changes in branch c"
        }
      }
    }
  }
}
