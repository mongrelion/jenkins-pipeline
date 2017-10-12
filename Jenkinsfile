pipeline {
  agent any

  stages {
    stage("Build") {
      steps {
        echo "Building the container image"
        sh "echo make image"
      }
    }

    stage("Test") {
      steps {
        echo "Running unit tests"
        sh "echo make test"
      }
    }

    stage("Push") {
      steps {
        echo "Pushing container image to ECR"
        sh "echo make push"
      }
    }
  }
}
