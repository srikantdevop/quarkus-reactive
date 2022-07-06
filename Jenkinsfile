pipeline {
    agent any
        stages {
        stage('Clone Repo') {
            steps {
                checkout scm
            }
        }
        stage('Build Image') {
            steps {
                //sh 'docker build -t raj80dockerid/jenkinstest ./pushdockerimage/' (this will use the tag latest)
		sh 'mvn clean package'
            }
        }
        
        }
    
    }
