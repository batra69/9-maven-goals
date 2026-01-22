pipeline {
    agent any

    environment {
        MVN = "/opt/homebrew/bin/mvn"
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/batra69/9-maven-goals.git'
            }
        }

        stage('Maven Validate') {
            steps { sh '$MVN validate' }
        }

        stage('Maven Compile') {
            steps { sh '$MVN compile' }
        }

        stage('Maven Test') {
            steps { sh '$MVN test' }
        }

        stage('Maven Package') {
            steps { sh '$MVN package' }
        }

        stage('Maven Verify') {
            steps { sh '$MVN verify' }
        }

        stage('Maven Install') {
            steps { sh '$MVN install' }
        }

        stage('Maven Deploy') {
            steps { sh '$MVN deploy -DskipTests || true' }
        }

        stage('Maven Clean') {
            steps { sh '$MVN clean' }
        }

        stage('Maven Site') {
            steps { sh '$MVN site || true' }
        }
    }
}
