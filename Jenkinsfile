pipeline {
    agent any

    environment {
        SONARQUBE_SERVER = 'LocalSonar'          // Nom configuré dans Jenkins → Manage Jenkins → SonarQube
        SONARQUBE_TOKEN = 'sqp_9ab21b4325c1dcb4b2827793e6d0e128ecd24125'          // ID du "Secret text" contenant le token
        DOCKER_IMAGE_NAME = 'monapp:latest'      // Nom de l'image Docker à construire
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

     
        
        
    }
}
