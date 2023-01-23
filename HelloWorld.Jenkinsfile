pipeline {
  agent any

  stages {
    stage ('Git-Checkout') {
      steps {
        echo "Checking out project from Git repo...";
        git clone https://github.com/invimagit/devopsHelloWorld.git
      }
    }

    stage ('Build') {
      steps {
        echo "Building the checked-out project...";
      }
    }

    stage ('Test-Units') {
      steps {
        echo "Running Unit Tests...";
      }
    }

    stage ('Quality-Gate') {
      steps {
        echo "Verifying Quality Gate...!";
      }
    }

    stage ('Deploy') {
      steps {
        echo "Deploying artifacts";
      }
    }
  }

  post {
    always {
      echo "This will always run";
    }
    success {
      echo "This will always run IF it was successful";
    }
    failure {
      echo "This will always run IF it failed";
    }
    unstable {
      echo "This will always run IF it was marked as unstable";
    }
    changed {
      echo "This will always run IF the state of the pipeline is different...For example, if the pipeline was previously failing but is now successful";
    }
  }
}
