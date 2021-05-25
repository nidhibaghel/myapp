pipeline {
    agent any

    stages {
        stage('Verify Branch') {
            steps {
                pwsh(script: 'Write-Output "$GIT_BRANCH"'')
            }
        }
        
    }
}

