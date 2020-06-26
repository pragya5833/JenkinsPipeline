pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
        archiveArtifacts 'target/*.jar'
        junit 'target/surefire-reports/*.xml'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

  }
}