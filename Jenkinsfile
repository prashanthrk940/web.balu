  node('master') {
    properties([
     [$class: 'BuildDiscarderProperty', 
        strategy: [
          $class: 'LogRotator', 
          daysToKeepStr: '10'
        ]
      ]
    ])

    stage('Checkout') {
      git 'https://github.com/Balu423/Web.git'
    }

    stage('Build') {
        sh 'mvn clean package'
    }
  }
