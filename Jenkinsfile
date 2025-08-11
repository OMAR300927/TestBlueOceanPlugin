pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

        stage('test1') {
          steps {
            echo 'Running Test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure deploy?', ok: 'Yes, I am sure')
        echo 'Deployment Complete'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build completed'
      }
    }

  }
}