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

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv("${SONARQUBE_SERVER}") {
                    sh """
                    sonar-scanner \
                      -Dsonar.projectKey=monapp \
                      -Dsonar.sources=. \
                      -Dsonar.host.url=$SONAR_HOST_URL \
                      -Dsonar.login=${SONARQUBE_TOKEN}
                    """
                }
            }
        }

        
        }
    }
}
