pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            sh 'echo "This is stage1"'
          }
        }

        stage('stage1.1') {
          steps {
            sh '''sleep 5
echo "This is parallel stage1.1"'''
          }
        }

        stage('stage1.2') {
          steps {
            sh '''sleep 5
echo "This is stage1.2"'''
          }
        }

      }
    }

    stage('stage2') {
      steps {
        sh 'echo "This is stage2"'
      }
    }

  }
}