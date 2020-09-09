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
            utesterstartscan baseAddress: 'https://www.user1st.com', errorsHigh: '', errorsLow: '', errorsMedium: '', errorsSuggestions: '', project: 'Tom', scanSettingsId: 'd7984f4f-2804-41f8-9db0-c56fbe12c141'
            sleep 20
          }
        }

      }
    }

    stage('uTester Scan') {
      steps {
        utesterstartscan baseAddress: 'https://www.user1st.com', errorsHigh: '', errorsLow: '', errorsMedium: '', errorsSuggestions: '', project: 'Tom', scanSettingsId: 'd7984f4f-2804-41f8-9db0-c56fbe12c141'
        sleep 20
      }
    }

  }
}
