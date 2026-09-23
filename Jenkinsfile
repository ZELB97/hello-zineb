pipeline {
    agent any 
    stages {
        stage('clone') { 
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/bigvaluesys/hello.git"
            }
        }
        stage('build') { 
            steps {
                sh "cd hello/ && javac --release 21 bvs.java"
            }
        }
        stage('run') { 
            steps {
                sh "cd hello/ && java bvs"
            }
    
        }
    stage('Hello'){
        steps {
            sh "echo Hello zineb !"
        }
    }
        
    }
    
}
