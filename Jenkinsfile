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
      git branch: 'Dev', url: 'https://github.com/Balu423/Web.git'
      git branch: 'Dev', poll: true, url: 'https://github.com/Balu423/Web.git'
    }

    stage('Build') {
        sh 'mvn clean package'
    }
}
