pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh 'javac --release 21 bvs.java'
            }
        }

        stage('run') {
            steps {
                sh 'java bvs'
            }
        }

        stage('Hello') {
            steps {
                sh 'echo "Hello Zineb !"'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                script {
                    def scannerHome = tool 'SonarScanner'

                    withSonarQubeEnv('SonarQube') {
                        sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=."
                    }
                }
            }
        }
    }
}
