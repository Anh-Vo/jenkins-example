pipeline {
  agent any

  stages {
    stage ('Compile Stage') {
      steps {
        withMaven(maven : 'maven_3_6_0') {
          echo 'Running Maven Compilation...'
          sh 'mvn clean compile'
        }
      }
    }
    stage ('Testing Stage') {
      steps {
        withMaven(maven : 'maven_3_6_0') {
          echo 'Running Maven Test...'
          sh 'mvn test'
        }
      }
    }
    stage ('Deployment Stage') {
      steps {
        withMaven(maven : 'maven_3_6_0') {
          echo 'Running Maven Deployment...'
          sh 'mvn deploy'
        }
      }
    }
  }
}