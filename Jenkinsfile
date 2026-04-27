pipeline {
    agent any
        stages {
            stage ("GIT") {
                staps {

                git ""
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
