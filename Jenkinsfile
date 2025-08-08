pipeline {
  /* use the official Gradle image, which bundles Gradle 6.0.1 + JDK 11 */
  agent {
    docker {
      image 'gradle:6.0.1-jdk11'
      args  '-v $HOME/.gradle:/home/gradle/.gradle'
    }
  }
  stages {
    stage('Build') {
      steps {
        /* we’re already in the workspace root; go into “complete” */
        dir('complete') {
          sh './gradlew clean build'
        }
      }
    }
  }
}
