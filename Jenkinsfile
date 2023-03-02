pipeline{
    agent any

    tools {
        maven "Maven"
    }
    stages{

       stage("Clone code from VCS") {
            steps {
                script {
                    git 'https://github.com/wissem007/scrum-board.git';
                }
            }
        }
        
        stage("verfier version docker"){
            steps{
                sh '''docker version
docker info
docker compose version
curl --version'''
           
        }
    }
        stage("Run Docker Compose"){
            steps{
                sh '''cd /var/lib/jenkins/workspace/dockercompose
docker-compose down
docker-compose up -d
docker ps'''
           
        }
    }
   
}
}
