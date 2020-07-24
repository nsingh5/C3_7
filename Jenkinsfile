pipeline {
    agent any

    stages {
        stage ('Initialize') {
            steps {
               echo "initailting"
               git "https://github.com/nsingh5/maven.git/"
            }
        }

        stage ('Build') {
            steps {
               bat "dir"
              bat "mvn install -DskipTests"
               //fortifyClean addJVMOptions: '', buildID: 'test', logFile: '', maxHeap: ''
            }
            post {
                success {
                   echo "passed"
                }
            }
        }
    }
}
