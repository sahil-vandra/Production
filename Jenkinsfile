AWS_ACCOUNT_ID="997817439961"
AWS_DEFAULT_REGION="ap-south-1" 
IMAGE_REPO_NAME="sahil-demo"
IMAGE_TAG="prod-img_${GIT_COMMIT}"
CLUSTER_NAME="Production-Cluster"
SERVICE_NAME="Prod-Service"
TASK_DEFINITION_NAME="Production"
DESIRED_COUNT="1"

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 997817439961.dkr.ecr.ap-south-1.amazonaws.com
