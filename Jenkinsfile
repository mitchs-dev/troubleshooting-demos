pipeline {
    agent {
       node { label 'MyAgent' }
    }
    environment { 
        version =  '16.5'
    }
    options {
        timestamps()
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }    
        stage ('Build and test'){
            steps {
		sh 'ls -la'
                sh 'chmod +x runScript.sh'
		sh './runScript.sh'
            }
        }
    }
}
