@Library('php-lint') _

pipeline {
  agent any

  stages {
    stage ("Checkout") {
      steps {
        echo("hello")
      }
    }
    stage("Build") {
      steps {
        sh(libraryResource('com/example/php-lint.sh'))
      }
    }
  }
}
