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
            post {
                success {
                    archiveArtifacts artifacts: 'dist/**/*', fingerprint: true
                }
            }
        }
        stage('Publish') {
          steps {
              script {
                  copyArtifacts(
                      projectName: currentBuild.projectName,
                      filter: 'dist/**/*',
                      target: '/var/jenkins_home/publish'
                  )
              }
          }
        }
    }
}
