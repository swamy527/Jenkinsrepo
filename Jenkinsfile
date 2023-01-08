pipeline {
    agent any
    tools {
        maven "apache-maven-3.8.7"
    }
    stages {
       
       stage('maven version') {
            steps {
            sh 'mvn --version'
       }
       }
       stage('git clone') {
            steps {
            git branch: 'main', url: 'https://github.com/swamy527/project.git'
       }
       }
       stage('maven clean') {
            steps {
            sh 'mvn clean'
       }
       }
       stage('code validate') {
            steps {
            sh 'mvn validate'
       }
       }
       stage('maven test') {
            steps {
            sh 'mvn test'
       }
       }
       stage('code package') {
            steps {
            sh 'mvn package'
       }
       }
       stage('code deploy') {
            steps {
            sh 'mvn deploy'
       }
       }
}
}