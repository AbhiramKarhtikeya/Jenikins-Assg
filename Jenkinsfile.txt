pipeline {
  agent { label 'docker-agent' }
  stages {
    stage('Checkout') {
      steps { checkout scm }
    }
    stage('Echo') {
      steps {
        echo "Name: Sanjay Varma"
        echo "Roll: AI006"
      }
    }
    stage('Test') {
      steps {
        sh 'python3 --version'
      }
    }
  }
}
