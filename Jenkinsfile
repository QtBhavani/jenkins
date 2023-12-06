pipeline {
  agent { label 'agent' }
    tools {
      jdk 'java17'
      maven 'maven3'
    }
  stages {
    stage("checkout from SCM"){
      steps {
        git branch: 'main', credentialsId: 'githubtoken', url: 'https://github.com/QtBhavani/jenkins.git'
      }
}
    stage("Build Application"){
      steps {
        sh "mvn clean package"
      }
}
    stage("Test Application"){
      steps {
        sh "mvn test"
      }
    }
  }
}

