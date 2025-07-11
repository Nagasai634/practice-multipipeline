pipeline {
    agent {
        label 'jenkins-slave'  
    }
    tools {
        jdk 'jdk'             
        maven 'maven'         
    }
    stages {
        stage('Build') {      
            steps {
                
                cleanWs()
                
                // Clone repository using Jenkins git step instead of shell
                git 'https://github.com/devopswithcloud/sample-maven.git'
                
                // Build with proper error handling
                dir('/home/nagasaivardhan724/sample-maven') {
                    sh "mvn clean package"
                }
            }
            
        }
    }
}
