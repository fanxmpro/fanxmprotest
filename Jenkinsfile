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

    stage('build') {
      steps {
        sh 'sudo -H pip install -r requirements.txt'
      }
    }

    stage('run') {
      agent {
        node {
          label '1'
        }

      }
      steps {
        sh 'python app.py'
      }
    }

  }
}