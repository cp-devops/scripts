pipeline {
  agent any
  stages {
    stage('Lint HTMl') {
      steps{
      sh 'echo "test file"'
      sh 'tidy -q -e *.html'
      }
    }
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-1', credentials:'aws-static'){
          sh 'echo "Uploaded index file to devops-cp bucket">hello.txt'
          s3Upload(file:'index.html', bucket:'devops-cp-jenkins')
        } 
      }
    }

  }
}
