pipeline {
  agent none
  stages {
    stage('build') {
      steps {
        sh '''pwd 
date'''
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