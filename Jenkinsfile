pipeline {
    agent
    {
        node {
                label 'master'
                customWorkspace "${env.JobPath}"
              }
    }

    stages 
    {
        stage('Start') {
            steps {
                sh 'ls'
            }
        }

        stage ('Invoke_pipeline') {
            steps {
                build job: 'TEST_PRJ1', parameters: [
                string(name: 'param1', value: "value1")
                ]
            }
        }

        stage('End') {
            steps {
                sh 'ls'
                sh 'pwd'
                sh 'hostname'
            }
        }
    }
}
