pipeline {
  agent none
  stages {
    stage('Testing') {
      when {
        beforeAgent true
        anyOf {
          branch 'master'
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
}