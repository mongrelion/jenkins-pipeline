pipeline {
  agent any

  environment {
    DOCKER_USER = credentials("DOCKER_USER")
    DOCKER_PASS = credentials("DOCKER_PASS")
  }

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
        echo "Logging in with Docker"
        sh "echo docker login -u $DOCKER_USER -p $DOCKER_PASS"
      }
    }
  }
}
