pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                pwsh(script: 'Write-Output "$GIT_BRANCH"'')
            }
        }

        stage('Docker build Image') {
            steps {
                pwsh(script: 'docker image ls')
                pwsh(script: """
                cd C:\Users\Nidhi.Baghel.ASIA-PAC\Documents\Docker\Jenkins\myapp
                docker image -a 
                docker build -t myapp:v1 .
                cd ..
                """")
            }
        }
        
    }
}