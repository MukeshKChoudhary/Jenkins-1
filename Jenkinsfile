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
        archiveArtifacts '**/*.txt'
        sh 'echo "FOO Credentials is : $FOO"'
        sh 'echo "FOO_USR is $FOO_USR"'
        sh 'echo "FOO_PSW is $FOO_PSW"'
      }
    }

  }
  environment {
    SOME_VAR = 'MUKESH_KC'
    INBETWEEN = 'Something in between'
    OTHER_VAR = "${SOME_VAR}"
    CRED1 = credentials('cred1123')
    CRED2 = credentials('b1f8951a-578c-43ee-b02c-570da062edfc')
    FOO = credentials('b1f8951a-578c-43ee-b02c-570da062edfc')
  }
}