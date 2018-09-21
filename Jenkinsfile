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
            build(job: 'myProject', quietPeriod: 1)
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