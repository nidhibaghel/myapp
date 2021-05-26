pipeline {
  agent any
  triggers {
    GenericTrigger(
     genericVariables: [
      [key: 'ref', value: '$.ref'],
      [key: 'repository', regexpFilter: '[^a-z_-]', value: '$.repository']
     ],
     causeString: 'Triggered on $ref',
     regexpFilterExpression: 'myapp refs/heads/' + BRANCH_NAME,
     regexpFilterText: '$repository $ref',
     printContributedVariables: true,
     printPostContent: true
    )
  }

  stages {
    stage('Test Generic Trigger') {
      steps {
        sh """
          echo Variables from shell:
          echo reference ${ref}
          echo repository ${repository}
        """
      }
    }
  }
}