node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarQube Scanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonarqube-scanner"
    }
  }
}
