pipeline {
  agent any

  stages {
    stage("build"){
      steps {
        echo 'building the app'
        systemctl status jenkins
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
