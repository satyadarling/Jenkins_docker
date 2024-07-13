pipeline {
    agent { label 'amazon-slave' }
    tools {
        maven 'Maven 3.9.8' // Replace with your Maven installation name
    }
    stages {
        stage('Build') {
            steps {
                script {
                    withEnv(["PATH+MAVEN=${tool 'Maven 3.9.8'}/bin"]) {
                        sh 'mvn -B clean verify'
                    }
                }
            }
        }
    }
}
