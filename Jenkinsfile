pipeline {
    agent {
        node: 
          label 'Jenkins_Node'
     }
    tools {

        maven 'maven 3.6.3'
        jdk 'jdk 11.0.16'
    }
    stages {
        stage('Check Maven Version') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('Check Java Version') {
            steps {
                sh 'java -version'
            }
        }
        stage('Validate the code') {
            steps {
                sh 'mvn validate'
            }
        }
         stage('Compile the code') {
            steps {
                sh 'mvn compile'
            }
        }
         stage('Test the code') {
            steps {
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
