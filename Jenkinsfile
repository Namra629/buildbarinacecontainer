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
                
                sh '''
        
        mkdir -p /home/Namra/SimpleWeather-Android/bars

docker run --rm -d -e LICENSE=accept -v /home/Namra/SimpleWeather-Android:/home/ace/project ibmcom/ace-mqclient:latest 
bash -c " ibmint package --input-path /home/ace/project --output-bar-file /home/ace/project/bars/SimpleWeather.bar"
                '''

                
            }
        }
    }

    
}
    
            


















