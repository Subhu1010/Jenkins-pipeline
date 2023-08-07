pipeline {
  agent none
  stages {
    stage('build') {
      steps {
        sh '''echo "hello world"
pwd
whoami'''
      }
    }

    stage('teststage') {
      parallel {
        stage('test') {
          steps {
            echo 'test is done'
          }
        }

        stage('testpar') {
          steps {
            echo 'test parallel'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy the project'
        sleep 30
      }
    }

  }
}