pipeline {
    agent {
        label 'jenkins-slave'  // Make sure this label exists on your agent/node
    }
    tools {
        jdk 'jdk'             // Must match EXACT name from Jenkins Global Tool Configuration
        maven 'maven'         // Must match EXACT name from Jenkins Global Tool Configuration
    }
    stages {
        stage('Build') {      // Changed to capitalize stage name (convention)
            steps {
                // Clean workspace more safely
                cleanWs()
                
                // Clone repository using Jenkins git step instead of shell
                git 'https://github.com/devopswithcloud/sample-maven.git'
                
                // Build with proper error handling
                dir('/home/sai/jenkins/workspace/pipeline3/sample-maven') {
                    sh "mvn clean package"
                }
            }
            
        }
    }
}
