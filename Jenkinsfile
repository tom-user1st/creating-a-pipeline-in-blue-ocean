pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('uTester Scan') {
      steps {
        utesterstartscan(project: 'Tom', scanSettingsId: 'd7984f4f-2804-41f8-9db0-c56fbe12c141', baseAddress: 'https://www.user1st.com')
      }
    }

  }
}