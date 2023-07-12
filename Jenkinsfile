pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://3.110.111.18:9000 \\
  -Dsonar.token=sqp_147fa778c085c2c4105db64bcf6eda5d7f1e5a2e'''
      }
    }

  }
}