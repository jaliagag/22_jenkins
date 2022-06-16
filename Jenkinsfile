//CODE_CHANGES = GetGitChanges() // groovy script to check value of boolean

pipeline {
  agent any

  environment { // create environment variable
    NEW_VERSION = '1.0.0'
//    SUDO_CREDENTIALS = credentials('sudo') // instead of storing credentials globally, we can use it on an individual job
  }
  stages {
    stage("build"){
 //     when {
 //       expression {
 //         BRANCH_NAME == 'dev' && CODE_CHANGES == true
 //       }
 //     }
      steps {
        echo 'building the app'
        echo "building version ${NEW_VERSION}" // variable in string must be in ""
        withCredentials([
          usernamePassword(credentials: 'sudo', usernameVariable: USER, passwordVariable: PWD)
          // created 2 variables from sudo credentials, USER n PWD
        ]) {
          echo "${USER} ${PWD}"

        }
        echo "creds ${SUDO_CREDENTIALS}"
        sh "${SUDO_CREDENTIALS}"
        
        // sudo apt install keybase
        // keybase pgp gen

        //sh 'npm install'
        //sh 'npm build'
      }
    }

    stage("test"){
      when {
        expression {
          env.BRANCH_NAME == 'dev' // only executes if branch is dev

          // BRANCH_NAME == 'dev' || BRANCH_NAME == 'master'
          // or BRANCH_NAME
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

//  post { // after all steps are done
//    always {
//      // either success or fail
//      // send email? 
//    }
//    success { // only relevant if the build succeeds
//      
//    }
//    failure {
//
//    }
//  }
}
