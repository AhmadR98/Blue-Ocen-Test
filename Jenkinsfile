pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed '
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Test1 completed'
          }
        }

        stage('Test2') {
          steps {
            echo 'Test2 completed'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to complete this stage ?', ok: 'Yes , I am sure ')
        echo 'Deploy completed'
      }
    }

    stage('Notify for  new build') {
      steps {
        echo 'New build completed successfully'
      }
    }

  }
}