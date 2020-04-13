pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-1', credentials:'aws-static'){
          sh 'echo "hello KB">hello.txt'
          s3Upload(file:'index.html', bucket:'devops-cp-jenkins')
        } 
      }
    }

  }
}
