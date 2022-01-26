pipeline {
  agent any
  stages {
    stage('print message') {
      steps {
        echo 'Consegui completar um passo da pratica!!!'
        mail(subject: 'iniciando pipeline', body: 'iniciando pipeline', to: 'Ruandgn@alu.ufc.br')
      }
    }

    stage('test') {
      steps {
        echo 'vamos testar'
        sleep 15
        build(job: 'PRATICA 5 GC', propagate: true)
      }
    }

    stage('Deploy') {
      steps {
        VersionNumber(skipFailedBuilds: true, versionPrefix: '1.0', versionNumberString: '1,0')
      }
    }

  }
}