node {
  stage('SCM') {
    checkout scm
  }
  stage('') {
    bat 'echo gg.c'
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonarqube';
    withSonarQubeEnv() {
      bat "${scannerHome}/bin/sonar-scanner"
    }
  }
}
