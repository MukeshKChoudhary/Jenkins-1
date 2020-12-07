pipeline {
  agent any
  stages {
    stage('Printing Variables') {
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
    SOME_VAR = 'MUKESH_KC'
    INBETWEEN = 'Something in between'
    OTHER_VAR = "${SOME_VAR}"
    CRED1 = credentials('cred1')
    CRED2 = credentials('cred1')
  }
}