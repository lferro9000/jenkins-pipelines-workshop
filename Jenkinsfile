@Library('php-lint') _

pipeline {
  agent any

  stages {
    stage ("Checkout") {
      steps {
        checkout scm
      }
    }
    stage("Composer") {
      steps {
        sh('composer install')
      }
    }
    stage("Build") {
      steps {
        sh(libraryResource('com/example/php-lint.sh'))
      }
    }
  }
}
