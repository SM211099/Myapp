pipeline {
    agent any
        stages {
            stage ("GIT") {
                staps {

                git "https://github.com/SM211099/Myapp.git"
            }
        
            stage ("Compose") {

                sh "docker compose up"
            }
        
            stage ("Docker-Build") {

                sh "docker build -t myapp ."
            }

            stage ("Docker-run") {

                sh "docker run -itd myapp"
            }
        
        } 
            
    }

} 
