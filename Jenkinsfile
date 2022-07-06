pipeline {
    agent any
    environment{
        
    }
    stages {
        stage('Clone Repo') {
            steps {
                checkout scm
                sh 'ls *'
            }
        }
        stage('Build Image') {
            steps {
                //sh 'docker build -t raj80dockerid/jenkinstest ./pushdockerimage/' (this will use the tag latest)
		sh './mvnw clean package'
            }
        }
        
        }
    
    }
