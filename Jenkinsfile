pipeline {
  agent any
  tools{
      maven 'maven-job'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
        archiveArtifacts 'target/*.jar'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
        junit 'target/surefire-reports/*.xml'
      }
    }

  }
}