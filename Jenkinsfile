pipeline {
    agent any

    stages {

        stage("GIT") {
            steps {
                sh "git clone https://github.com/SM211099/Myapp.git"
            }
        }

        stage("Compose") {
            steps {
                sh "docker compose up"
            }
        }

        stage("Docker-Build") {
            steps {
                sh "docker build -t myapp ."
            }
        }

        stage("Docker-run") {
            steps {
                sh "docker run -itd myapp"
            }
        }

    }
}
