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
                    
    docker.image('ibmcom/ace-mqclient:latest').inside("-v /home/Namra/SimpleWeather-Android:/home/ace/project") {
    sh '''
    echo "Building ACE BAR file..."
    mkdir -p /home/ace/project/bars
    ibmint package --input-path /home/ace/project --output-bar-file /home/ace/project/bars/SimpleWeather.bar
    echo "BAR build complete."
    '''
}

                }
            }
        }
    }
}


