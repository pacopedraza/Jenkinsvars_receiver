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
                sh "pwd"
                sh "ls"
                }
            }
        }
}
