pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.busybox'
    }

  }
  stages {
    stage('error') {
      steps {
        echo 'busybox /etc print'
      }
    }

  }
}