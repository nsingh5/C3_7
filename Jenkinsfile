pipeline {
    agent any
    tools { 
        maven 'Maven 3.6.3' 
        jdk 'jdk8' 
    }
    stages {
       
        
        stage ('Initialize') {
            steps { 
                git "https://github.com/nsingh5/C3_7.git/"
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                 
            }
        }
        stage ('Build') {
            steps {
                bat 'mvn -DskipTests install' 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
