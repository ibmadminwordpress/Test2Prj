pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "WELCOME to Build Stage"'
        echo 'Welcome to Print Message'
      }
    }
    stage('Test') {
      agent any
      environment {
        NAME = 'Srinivasan'
      }
      steps {
        sh 'ping -a drapp03.i21.com'
      }
    }
    stage('Deploy') {
      steps {
        sh '''echo " Deploy stage"
echo $NAME'''
      }
    }
  }
  environment {
    MYNAME = 'Srinivasan'
    JOB = 'Engg.'
  }
}