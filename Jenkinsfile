pipeline {
  agent {
    docker {
      image 'node:8-alpine'
    }

  }
  stages {
      
    stage('wellcome') {
      steps {
        sh 'echo "wellcome to dojo 2 !"'
      }
    }
    stage('install') {
      steps {
        sh 'npm install'
      }
    }

  }
  post {
    success {
        sh 'node dojo/dojo2_fin.js'
    }
  }  
  environment {
    npm_config_cache = 'npm-cache'
    HOME = '.'

  }
}