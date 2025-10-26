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
        mkdir -p /home/Namra/ACE-HelloWorld-main-1/bars

docker run -d --rm  -e LICENSE=accept --name acecontainer ibmcom/ace
ibmint package --input-path /home/Namra/ACE-HelloWorld-main-1
 --output-bar-file /home/Namra/ACE-HelloWorld-main-1/bar/Helloworld.bar"    '''

                
            }
        }
    }

    
}
    
            



































