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
      echo 'Pulling...' + env.BRANCH_NAME
    }

    stage('Build') {
        sh 'mvn clean package'
    }
}
