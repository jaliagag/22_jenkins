pipeline {
  agent any

  environment { // create environment variable
    NEW_VERSION = '1.0.0'
  }
  stages {
    stage("build"){
      steps {
        echo 'building the app'
        echo "building version ${NEW_VERSION}" // variable in string must be in ""
      }
    }

    stage("test"){
      when {
        expression {
          env.BRANCH_NAME == 'dev' // only executes if branch is dev

        }
      }
      steps {
        echo 'testing'

      }
    }

    stage("deploy"){
      steps {
        echo 'deploy'
      }
    }
  }
}
