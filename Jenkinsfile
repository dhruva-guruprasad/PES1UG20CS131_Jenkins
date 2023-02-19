pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ task5.cpp -o prgm'
        sh 'make -C main'
        build job: 'PES1UG20CS131-1', wait: true
        echo 'PES1UG20CS131-1 build successful'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh './prgm'
        echo 'Test Stage Successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy Stage Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
