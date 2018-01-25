pipeline {
    agent any
    stages {
     stage('Copy Archive') {
         steps {
             script {
                 step ([$class: 'CopyArtifact',
                 projectName: 'e2e_pip',
                 filter: "hw.sh",
                 target: 'Artifacts']);
             }
         }
     }
}
