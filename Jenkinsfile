pipeline {
    agent {
        label 'jenkins-slave'
    }
    tools {
        jdk 'jdk'
        maven 'maven'
    }
    stages {
        stage('build') {
            steps {
                sh "java --version"
                sh "mvn --version"
            }
        }
    }
}
