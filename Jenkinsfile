pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/narendrasingamaneni91/ecommerce.git'
      }
    }
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            sh 'sh compile'
          }
        }
        stage('test') {
          steps {
            sh 'sh test'
          }
        }
      }
    }
  }
}