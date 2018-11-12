pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v $HOME/.m2:/root/.m2:z -u root'
            reuseNode true 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package .' 
            }
        }
    }
}