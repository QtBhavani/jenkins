pipeline {
  agent { label 'agent' }
    tools {
      jdk 'java17'
      maven 'maven3'
    }
  stages{
    stage("cleanup workspace"){
      steps {
        cleanWs()
      }
}
    stage("checkout from SCM"){
      steps {
        git branch: 'main', credentialsID: 'github', url: 'https://github.com/QtBhavani/jenkins.git'
      }
}
    stage("Build Application"){
      steps {
        sh "mvn clean package"
      }
}
    tage("Test Application"){
      steps {
        sh "mvn test"
      }
    }
  }
}
