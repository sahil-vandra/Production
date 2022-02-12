pipeline {
    agent any

    environment {
        AWS_ACCOUNT_ID="997817439961"
        AWS_DEFAULT_REGION="ap-south-1" 
        IMAGE_REPO_NAME="sahil-demo"
        IMAGE_TAG="prod-img"
        CLUSTER_NAME="Production-Cluster"
        SERVICE_NAME="Prod-Service"
        TASK_DEFINITION_NAME="Production:1"
        DESIRED_COUNT="1"
        registryCredential = "AWSCred"
        REVISION =  "1"
        REPOSITORY_URI = "${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"
    }
    
    stages {
        stage('Trigger pipeline and clone code ') {
            steps {
                echo 'Someone push code on git.'
                git branch: 'prod', url: 'https://github.com/sahil-vandra/Production.git'
            }
        }
                
    }
}
