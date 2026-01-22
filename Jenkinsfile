pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK17'
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/batra69/9-maven-goals.git'
            }
        }

        stage('Maven Validate') {
            steps { sh 'mvn validate' }
        }

        stage('Maven Compile') {
            steps { sh 'mvn compile' }
        }

        stage('Maven Test') {
            steps { sh 'mvn test' }
        }

        stage('Maven Package') {
            steps { sh 'mvn package' }
        }

        stage('Maven Verify') {
            steps { sh 'mvn verify' }
        }

        stage('Maven Install') {
            steps { sh 'mvn install' }
        }

        stage('Maven Deploy') {
            steps { sh 'mvn deploy -DskipTests || true' }
        }

        stage('Maven Clean') {
            steps { sh 'mvn clean' }
        }

        stage('Maven Site') {
            steps { sh 'mvn site || true' }
        }
    }
}
