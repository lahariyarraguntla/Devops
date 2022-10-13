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
      parallel {
        stage('stage2') {
          steps {
            sh 'echo "This is stage2"'
            sh 'echo "stage2"'
          }
        }

        stage('stage2.1') {
          steps {
            sh 'echo "stage2.1"'
          }
        }

        stage('stage2.2') {
          steps {
            sh 'echo "stage2.2"'
          }
        }

        stage('stage2.3') {
          steps {
            sh 'echo " hi stage2.3"'
          }
        }

      }
    }

    stage('stage3') {
      steps {
        sh 'echo "this is stage3"'
      }
    }

  }
}