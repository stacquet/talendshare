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
            
          }
        )
      }
    }
  }
  environment {
    tata = 'titi'
  }
}