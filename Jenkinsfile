pipeline {
  agent any

  environment {
    DOCKER_USER = credentials("DOCKER_USER")
    DOCKER_PASS = credentials("DOCKER_PASS")
  }

  stages {
    stage("Fetch") {
      steps {
        echo "Cloning project"
      }
    }

    stage("Build") {
      steps {
        sh "./scripts/build.sh"
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
