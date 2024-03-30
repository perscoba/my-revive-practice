


pipeline {
    agent any

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
    }
}
