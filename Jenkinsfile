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
  post {
    always {
        recordIssues(
            qualityGates: [
                [criticality: 'FAILURE', integerThreshold: 10, threshold: 10.0, type: 'TOTAL_HIGH'], 
                [criticality: 'FAILURE', integerThreshold: 5, threshold: 5.0, type: 'NEW']
                ], 
                sourceCodeRetention: 'LAST_BUILD', 
                tools: [grype()]
        )
    }
}
}
