pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:’us-east-1', credentials:'aws-static') {
        s3Upload(file:'index.html', bucket:'devops-cp-jenkins')
        } 
      }
    }

  }
}
