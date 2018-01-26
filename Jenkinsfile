#!groovy
pipeline {
        agent { node {label 'ecs' } }
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
}
