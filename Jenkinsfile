pipeline {
    agent any
    tools {
        nodejs '22.11.0'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
                sh 'npm run build'
            }
        }
        stage('Publish') {
          steps {
              archiveArtifacts artifacts: 'dist/**/*', fingerprint: true
          }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
