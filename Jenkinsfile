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
        sh 'echo " Today Date is   `date` "'
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