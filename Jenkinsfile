pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }

        stage('uTester Scan - Github') {
          steps {
            utesterstartscan(scanSettingsId: 'd7984f4f-2804-41f8-9db0-c56fbe12c141', project: 'Tom', baseAddress: 'https://github.com')
          }
        }

      }
    }

    stage('uTester Scan') {
      steps {
        utesterstartscan(project: 'Tom', scanSettingsId: 'd7984f4f-2804-41f8-9db0-c56fbe12c141', baseAddress: 'https://www.user1st.com')
        sleep 20
      }
    }

  }
}