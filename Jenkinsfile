pipeline {
  agent any

  tools {
    nodejs 'NodeJS' // Name of your Node.js installation
  }

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
          // Run unit tests
          sh 'npm test'
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          // Start the application
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
