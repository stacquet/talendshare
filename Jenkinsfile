pipeline {
  agent none
  stages {
    stage('sleep') {
      steps {
        sleep 3
      }
    }
    stage('sleep2') {
      steps {
        parallel(
          "sleep2": {
            sleep 5
            
          },
          "echo": {
            input(message: 'tata', id: 'tata', ok: 'tata')
            echo 'fini2'
            
          }
        )
      }
    }
    stage('suite') {
      steps {
        echo 'suite'
        sleep 2
      }
    }
  }
  environment {
    tata = 'titi'
  }
}