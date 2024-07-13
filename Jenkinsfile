pipeline {
    agent any
    tools {
        maven 'M3' // Use the correct Maven installation name
    }
    stages {
        stage('Build') {
            steps {
                script {
                    withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
                        sh 'mvn -B clean verify'
                    }
                }
            }
        }
    }
}
