pipeline {
  agent any
  stages {
    stage('prepare') {
      parallel {
        stage('prepare') {
          steps {
            echo 'this is to prepare'
          }
        }
        stage('prepare1') {
          steps {
            echo 'this is prepare 1'
          }
        }
      }
    }
    stage('build') {
      agent any
      steps {
        git(url: 'https://github.com/LuningDeng/jenkinsTest.git', branch: 'master', changelog: true)
      }
    }
  }
  environment {
    student = 'justin'
    teacher = 'morna'
  }
}