pipeline {
  agent any

  stages {
    stage("build"){
      steps {
        echo 'building the app'
        echo 'testfile' > letestfile
        //sh 'npm install'
        //sh 'npm build'
      }
    }
    stage("test"){
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
