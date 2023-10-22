pipeline {
    agent any

    triggers {
        pollSCM('*/1 * * * *') // Vérifier toutes les 5 minutes
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Récupération du code source"
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build du projet"
                // Ajoutez les commandes de build ici
                // Par exemple : sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                echo "Déploiement du projet"
                // Ajoutez les commandes de déploiement ici
                // Par exemple : sh 'docker-compose up -d'
            }
        }
    }
}

