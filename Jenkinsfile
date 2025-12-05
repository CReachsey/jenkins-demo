pipeline {
    agent any // This means any available agent (or the main server) can run the job

    stages {
        // Stage 1: Checkout the code (This step is implicit when using an SCM like Git)
        stage('Welcome') {
            steps {
                echo 'Starting the Jenkins CI/CD process.'
                echo 'Checking out code from Git...'
            }
        }
        
        // Stage 2: Run a simple command
        stage('Run Shell Command') {
            steps {
                sh 'echo "Current date and time is $(date)"' // 'sh' runs a shell command
                sh 'ls -al' // List files to show the workspace content
            }
        }
        
        // Stage 3: Post-build actions (like sending notifications)
        stage('Finish') {
            steps {
                echo 'Pipeline completed successfully!'
            }
        }
    }
}