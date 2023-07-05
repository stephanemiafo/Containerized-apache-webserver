pipeline {
  agent any

  stages {    // EVERY BRANCH WILL GET 'Hello'
    stage('Hello') {
      steps {
        echo "hello"
      }
    }
    stage('cat README'){
      when {            //FOR ANY BRANCH THAT START WITH pract, cat README.
        branch "pract*"   // This stage is specific only to branches that start with pract.
      }
      steps {
        sh '''
          cat README
        '''  
      }
    }
  }
}
