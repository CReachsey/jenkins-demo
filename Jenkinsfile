pipeline {
    // 1. Define the agent as a Docker image (global level)
    agent {
        // Use the official Node.js image for the entire pipeline
        docker { 
            image 'node:20-alpine' 
            args '-u 0' // Fixes permission issues common in Docker on Linux/Mac
        }
    }

    stages {
        stage('Check Node Version') {
            steps {
                // These commands run INSIDE the node:20-alpine container
                sh 'node --version' 
                sh 'npm --version' 
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // If you had a package.json, this would install packages
                sh 'echo "Skipping npm install for this example..."'
            }
        }
        
        stage('Clean Up') {
            steps {
                echo 'Build environment is automatically cleaned up as the container exits.'
            }
        }
    }
}