pipeline {
    agent any 
    
    stages{
        stage("Clone Code"){
            steps {
                echo "Cloning the code"
                git url:"https://github.com/vishwanath0303/react_django_demo_app", branch: "main" 
            }
        }
        stage("Build and creating container"){
            steps {
                echo "Building the image"
            }
        }
        stage("Deploy"){
            steps {
                echo "Deploying the container"
                sh "docker-compose down && docker-compose up -d"
                
            }
        }
     }
 }
