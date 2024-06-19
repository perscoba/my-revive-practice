


pipeline {
    agent any
   options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '5', artifactNumToKeepStr: '5', daysToKeepStr: '5', numToKeepStr: '5')
  disableConcurrentBuilds abortPrevious: true
}
    stages {

        stage('ecr-login') {
  steps {
    // One or more steps need to be included within the steps block.
  }
}












        
        // stage('SonarQube Analysis') {
        //     steps {
        //         script {
        //             def scannerHome = tool 'sonar';
        //             withSonarQubeEnv() {
        //                 sh "${scannerHome}/bin/sonar-scanner"
        //             }
        //         }
        //     }
        // }

    //     stage("Quality Gate") {
    //             steps {
    //               timeout(time: 1, unit: 'HOURS') {
    //                 waitForQualityGate abortPipeline: true
    //               }
    //             }
    //           }  
    }
}
