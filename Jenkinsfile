pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        script {
          // Install dependencies
          sh 'npm install'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          // Run unit tests (add unit tests in Step 6)
          sh 'npm test'
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          // Deploy the application (e.g., start it using node)
          sh 'nohup node app.js &'
        }
      }
    }
  }

  post {
    always {
      echo 'Pipeline finished.'
    }
  }
}
