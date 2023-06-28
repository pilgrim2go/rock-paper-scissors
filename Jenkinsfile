pipeline {

  agent any

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')

  }

  stages {
      when {
        anyOf {
            branch 'master'
            branch "fix-*"
            branch "fix2-*"

            environment name: 'BUILD_ENV', value: 'prod'
        }
        

    }
    stage('Hello') {

      steps {

        sh '''

          echo "java -version"

        '''

      }

    }

    stage('cat README') 

      steps {

        sh '''

          cat README.md

        '''

      }

    }

  }

}