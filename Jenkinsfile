#!groovy
pipeline {
  agent any
  triggers { pollSCM('H/15 * * * *') }

  stages {
      stage('prepare') {
          steps {
              sh "chmod +x gradlew"
          }
      }
      stage('build') {
          steps {
              sh "./gradlew clean assembleDebug --stacktrace"
          }
      }
  }
}