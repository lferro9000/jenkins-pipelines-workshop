@Library('php-lint') _

pipeline {
  agent any

  stages {
    stage ("Checkout") {
      steps {
        checkout(
                        [$class: 'GitSCM', branches: [[name: '*/plugin']],
                         doGenerateSubmoduleConfigurations: false,
                         extensions: [],
                         submoduleCfg: [],
                         userRemoteConfigs: [[url: 'https://github.com/lferro9000/jenkins-pipelines-workshop']]]
        )
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
