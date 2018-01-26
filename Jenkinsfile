#!groovy
pipeline {
        agent { node {label 'ecs' } }
        stages {
            stage('Copy Artifact from previous job') {
                steps {
                    script {
                        step ([$class: 'CopyArtifact',
                        projectName: 'e2e_pip',
                        filter: "hw.sh",
                        target: 'Artifacts']);
                    }
                }
            }
            stage('Use Artifact'){
                steps {
                    sh 'echo "Is going to reverse the string artifact"'
                    sh 'pwd'
                    sh 'ls'
                    sh 'cd Artifacts'
                    sh 'bash reverse_artifact.sh "`cat hw.txt`"'
                }
            }
        }
}
