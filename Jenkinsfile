pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                
                git branch: 'main', url: 'https://github.com/Namra629/buildbarinacecontainer.git'
            }
        }
        stage('Build ACE BAR') {
            steps {
                script {
                    
                    docker.image('ibmcom/ace:11.0.0.6.3-amd64').inside {
                        sh '''
                        echo "Building ACE BAR file..."
                        ibmint package --input-path /home/Namra/ACE-HelloWorld-main/app --output-bar-file /home/Namra/SimpleWeather-Android/bars/
                        echo "BAR build complete."
                        '''
                    }
                }
            }
        }
    }
}

