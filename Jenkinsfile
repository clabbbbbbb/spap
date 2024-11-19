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
                  echo 'Project name: ${currentBuild.projectName}'
                  copyArtifacts(
                      projectName: currentBuild.projectName,
                      filter: '**/*',
                      target: '/var/jenkins_home/publish'
                  )

                  sh 'ls -al /var/jenkins_home/publish'
              }
          }
        }
    }
}
