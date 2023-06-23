node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'sonar-maven';
    withSonarQubeEnv() {
      + /var/jenkins_home/tools/hudson.tasks.Maven_MavenInstallation/sonar-maven/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=myproject
    }
  }
}
