pipeline {
  agent any
  stages {
    stage('Calculate Resources') {
      steps {
        echo 'step 1'
      }
    }
    stage('Build') {
      parallel {
        stage('Build Redhat') {
          steps {
            echo 'Building on Redhat'
          }
        }
        stage('Build Debian') {
          steps {
            echo 'building on debian'
          }
        }
        stage('Build Windows') {
          steps {
            echo 'build on windows'
          }
        }
      }
    }
    stage('Generate repos') {
      steps {
        echo 'Generate repos'
      }
    }
    stage('Test Redhat') {
      parallel {
        stage('Test Redhat') {
          steps {
            echo 'Test Redhat'
          }
        }
        stage('Test Debian') {
          steps {
            echo 'Test Debian'
          }
        }
        stage('Test Windows') {
          steps {
            echo 'Test Windows'
          }
        }
      }
    }
    stage('Promote SHA') {
      steps {
        echo 'Promote SHA'
      }
    }
  }
}