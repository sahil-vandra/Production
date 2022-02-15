pipeline {
    agent any

    environment {
        AWS_ACCOUNT_ID="997817439961"
        AWS_DEFAULT_REGION="ap-south-1" 
        IMAGE_REPO_NAME="dev-repo-sahil"
        IMAGE_TAG="dev-img_${GIT_COMMIT}"
        CLUSTER_NAME="dev-cluster-sahil"
        SERVICE_NAME="dev-service-sahil"
        TASK_DEFINITION_NAME="Developer-sahil"
        DESIRED_COUNT="1"
    }
    
    stages {
        
        stage('Pipeline Running') {
            steps {
                git branch: 'dev', url: 'https://github.com/sahil-vandra/Production.git'
                
                sh "chmod +x -R ${env.WORKSPACE}"
                sh "./script-dev.sh"
            }
        }
      
    }
}
