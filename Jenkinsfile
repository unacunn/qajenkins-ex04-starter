pipeline {
  agent any
  environment {
    registry = "ex04"
    dockerImage = ""
  }
  stages {
    stage("Docker Build") {
      steps {
        sh "echo 'Docker Build...'"
      }
    }
    stage("Scan Image") {
      steps {
        sh "echo 'Scan Image...'"
      }
    }
  }
}
