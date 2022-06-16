//CODE_CHANGES = GetGitChanges() // groovy script to check value of boolean

pipeline {
  agent any

  stages {
    stage("build"){
 //     when {
 //       expression {
 //         BRANCH_NAME == 'dev' && CODE_CHANGES == true
 //       }
 //     }
      steps {
        echo 'building the app'
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
