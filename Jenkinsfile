pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/srikantdevop/quarkus-reactive.git'
            }
        }
        stage('Build') {
            steps {
                bat './mvnw -V clean install -DskipTests -DskipITs -DskipDocs'
            }
        }
    }
    
    post {
        always {
            deleteDir()
        }
    }
}