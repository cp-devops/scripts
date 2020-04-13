pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:’us-east-1’,credentials:'jenkins') {
        s3Upload(file:'index.html', bucket:'devops-cp-jenkins')
        } 
      }
    }

  }
}
