pipeline {
  agent any
  stages {
    stage('dev') {
      steps {
        sh 'echo "start pipeline"'
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            build(job: 'new-date', quietPeriod: 1)
          }
        }
        stage('build') {
          steps {
            echo 'hello'
          }
        }
      }
    }
  }
}