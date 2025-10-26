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

                bash -c "
         
           # Source ACE environment
                source /home/Namra/ace-12.0.12.16/server/bin/mqsiprofile
        mkdir -p /home/Namra/SimpleWeather-Android/bars

docker run -d --rm  -e LICENSE=accept -v /home/Namra/SimpleWeather-Android:/home/ace/project ibmcom/ace
ibmint package --input-path /home/ace/project --output-bar-file /home/ace/project/bars/SimpleWeather.bar"    '''

                
            }
        }
    }

    
}
    
            

































