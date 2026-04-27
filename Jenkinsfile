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
                sh "cd /var/lib/jenkins/workspace/First && docker compose up"
            }
        }

        stage("Docker-Build") {
            steps {
                sh "cd /var/lib/jenkins/workspace/First && docker build -t myapp ."
            }
        }

        stage("Docker-run") {
            steps {
                sh "cd /var/lib/jenkins/workspace/First && docker run -itd myapp"
            }
        }

    }
}
