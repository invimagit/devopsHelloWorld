pipeline {
  agent {
    kubernetes {
      defaultContainer 'maven'
      yamlFile 'pod-template.yaml'
    }
  }
  stages {
    stage('Run maven') {
      steps {
        sh 'mvn -version'
      }
    }
  }
}
