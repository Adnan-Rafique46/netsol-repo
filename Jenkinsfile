pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''#!/bin/bash
echo "Hello, world!"
'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test'
          }
        }

        stage('test-par') {
          steps {
            echo 'test-par'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}