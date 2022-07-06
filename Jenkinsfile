pipeline {
    agent any
    triggers {
        cron('H H(13-14) * * *')
    }
    
    stages {
         stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/srikantdevop/quarkus-reactive.git'
            }
        }
        stage('Build') {
            steps {
                             
                             
                              sh './mvnw -V clean install -DskipTests -DskipITs -DskipDocs'
            }
        }
        }
    post {
        always {
            deleteDir()
        }
    }

}