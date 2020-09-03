pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/root/data') {
          git(url: 'https://github.com/fanxmpro/fanxmprotest/tree/master', credentialsId: 'fanxmpro@gmail.com', poll: true)
        }

      }
    }

  }
}