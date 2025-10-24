pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Get your code from GitHub repo
                git branch: 'main', url: 'https://github.com/your-org/your-repo.git'
            }
        }
        stage('Build ACE BAR') {
            steps {
                script {
                    // Use ACE container to run BAR build command
                    docker.image('ibmcom/ace-mqclient:latest').inside {
                        sh '''
                        echo "Building ACE BAR file..."
                        mqsicreatebar -data /home/ace/project -b MyApp.bar -a MyApp
                        echo "BAR build complete."
                        '''
                    }
                }
            }
        }
    }
}
