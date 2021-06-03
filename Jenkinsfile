pipeline {
    agent any

    stages {
        stage('Verify Branch') 
              {
            steps {
                pwsh(script: 'Write-Output "$GIT_BRANCH"')
                  }
            }
               stage('Docker build Image')
                   {
                steps {
                pwsh(script: 'docker image ls')
                pwsh(script: """
                     cd myapp/
                     docker images -a 
                     docker build -t myapp:v1
                     cd ..
                """)
                       }
                    }
        
         }

    }
