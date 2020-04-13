pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
            echo "Multi-line shell steps work"
            ls -lah
          '''
      }
    }

  }
}
