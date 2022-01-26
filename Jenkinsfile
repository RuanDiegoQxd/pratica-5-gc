pipeline {
  agent any
  stages {
    stage('print message') {
      steps {
        echo 'Consegui completar um passo da pratica!!!'
        mail(subject: '[passo 2] pratica 5', body: 'consegui realizar o segundo passo da pratica', to: 'Ruandgn@alu.ufc.br.com')
      }
    }

    stage('test') {
      steps {
        echo 'vamos testar'
        sleep 15
        build(job: 'pratica-5-gc', propagate: true)
      }
    }

  }
}