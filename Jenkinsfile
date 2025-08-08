pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        dir('complete') {
          // now running inside complete/, where gradlew lives
          sh './gradlew clean build'
        }
      }
    }
  }
}
