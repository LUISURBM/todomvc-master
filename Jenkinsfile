#!/usr/bin/env groovy

pipeline {
  agent any

  stages {
    stage('Test') {
      steps {
        echo 'Compile project'
        sh 'chmod +x gradlew && ./gradlew clean build -P env=prod'
      }
    }
    stage('Clean up') {
      steps {
        deleteDir()
      }
    }
  }
}