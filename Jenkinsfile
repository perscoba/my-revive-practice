


pipeline {
    agent any
   options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '5', artifactNumToKeepStr: '5', daysToKeepStr: '5', numToKeepStr: '5')
  disableConcurrentBuilds abortPrevious: true
}
    stages {
        
        stage('SonarQube Analysis') {
            steps {
                script {
                    def scannerHome = tool 'sonar';
                    withSonarQubeEnv() {
                        sh "${scannerHome}/bin/sonar-scanner"
                    }
                }
            }
        }

        stage("Quality Gate") {
                steps {
                  timeout(time: 1, unit: 'HOURS') {
                    waitForQualityGate abortPipeline: true
                  }
                }
              }  
    }
}
