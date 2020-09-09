pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''apt-get install -y curl \\
  && curl -sL https://deb.nodesource.com/setup_9.x | bash - \\
  && apt-get install -y nodejs \\
  && curl -L https://www.npmjs.com/install.sh | sh'''
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