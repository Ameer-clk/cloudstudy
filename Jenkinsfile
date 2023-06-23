node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Scanner') {
    def mvn = tool 'sonar-maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=myproject"
    }
  }
}
