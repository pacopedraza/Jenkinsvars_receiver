pipeline {
    agent any
    stages {
     stage('Copy Archive') {
         steps {
             script {
                 step ([$class: 'CopyArtifact',
                 projectName: '../End to End Testing/e2e_pip',
                 filter: "hw.sh",
                 target: 'Artifacts']);
             }
         }
     }
   }
}
