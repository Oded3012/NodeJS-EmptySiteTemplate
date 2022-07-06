pipeline {
  agent any
  stages {
    stage('checkout code') {
      parallel {
        stage('checkout code') {
          steps {
            git(url: 'git@github.com:Oded3012/NodeJS-EmptySiteTemplate.git', branch: 'master', credentialsId: 'jenkins-key')
          }
        }

        stage('say hello') {
          steps {
            sh 'echo "hello world"'
          }
        }

      }
    }

    stage('build') {
      steps {
        sh 'npm install'
      }
    }

  }
}