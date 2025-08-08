pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        // go into the project folder where gradlew lives
        dir('complete') {
          // run the wrapper directly
          sh './gradlew clean build'
        }
      }
    }
  }
}
