


pipeline {
    agent any
    triggers {
         githubPush()
    }
   options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '5', artifactNumToKeepStr: '5', daysToKeepStr: '5', numToKeepStr: '5')
  disableConcurrentBuilds abortPrevious: true
}
    stages {

      stage('build and push') {
            steps {
                sh " ls "
            }
        }  

      stage('ecr-login') {
           steps {
           sh " ls -l"
           dir('./new-dr') {
               sh "touch file.sh "
               sh " ls -l"

               script {
            if (fileExists('./file.sh')) {
                echo "file.sh found!"
            }
        }
           }
           
           }
     }


    // stage('Example Deploy') {
    //         when {
    //             branch 'main'
    //         }
            
    //       steps {
    //             sh " ls -l "
    //         }
    //     }






        
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
