pipeline {
  agent any
  environment {
    registry = "ex04"
    dockerImage = ""
  }
  stages {
    stage('Docker Build') {
      steps {
        script {
          dockerImage = docker.build(registry)
          dockerImage.tag("${registry}:${env.BUILD_NUMBER}")
        }
      }
    }
    stage('Scan Image') {
      steps {
        sh "echo 'Scan Image...'"
      }
    }
  }
}
