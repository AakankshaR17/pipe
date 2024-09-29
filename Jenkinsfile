pipeline {
    agent any

    tools {
        nodejs 'NodeJS' // Name of your Node.js installation in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }

        stage('Test') {
            when {
                expression {
                    fileExists('package.json') && sh(returnStdout: true, script: 'npm run | grep test').trim()
                }
            }
            steps {
                script {
                    sh 'npm test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Add your deployment commands here
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
