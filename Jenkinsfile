
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
   
}
}
