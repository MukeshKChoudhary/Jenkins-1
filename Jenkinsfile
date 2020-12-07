pipeline {
  agent any
  stages {
    stage('foo') {
      steps {
        sh 'echo "SOME_VAR is $SOME_VAR"'
        sh 'echo "INBETWEEN is $INBETWEEN"'
        sh 'echo "OTHER_VAR is $OTHER_VAR"'
        sh 'echo $CRED1 > cred1.txt'
        sh 'echo $CRED2 > cred2.txt'
        archive '**/*.txt'
      }
    }

  }
  environment {
    SOME_VAR = 'SOME VALUE'
    CRED1 = credentials('cred1')
    INBETWEEN = 'Something in between'
    CRED2 = credentials('cred2')
    OTHER_VAR = "${SOME_VAR}"
  }
}