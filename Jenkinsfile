pipeline {
  agent {
    node {
      label 'Docker-centos7'
    }

  }
  stages {
    stage('checkout code') {
      parallel {
        stage('checkout code') {
          agent {
            node {
              label 'Docker-centos7'
            }

          }
          steps {
            git(url: 'git@github.com:Oded3012/NodeJS-EmptySiteTemplate.git', branch: 'master', credentialsId: 'jenkins-key')
          }
        }

        stage('say hello') {
          agent any
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