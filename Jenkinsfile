pipeline {
  agent none
  stages {
    stage('Testing') {
      when {
        beforeAgent true
        anyOf {
          branch 'main'
        }
      }
      agent {
        label "php-7.4.16"
      }
      steps {
        unittest()
      }
    }
  }
  post {
    always {
      slackNotification(1)
    }
  }
}