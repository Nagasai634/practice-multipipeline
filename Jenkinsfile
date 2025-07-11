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
                sh "git clone https://github.com/devopswithcloud/sample-maven.git"
                sh "mvn clean package"
            }
        }
    }
}
