pipeline {
    agent any
         stages{
        stage ('Bulding docker docker image') {
            steps {
                echo "build docker image"
                sh 'sudo docker build --no-cache -t 010762572680.dkr.ecr.ap-south-1.amazonaws.com/kubernates .'
                sh 'sudo docker push 010762572680.dkr.ecr.ap-south-1.amazonaws.com/kubernates'
            }
        }
             
        stage ('Deployment') {
            steps {
                echo "Deployment"
                sh 'kubectl apply -f demo.yaml'
                sh 'kubectl apply -f demo-svc.yaml'
                sh 'kubectl rollout restart deployment/httpd-deployment'
            }
        }
        
}
  
}  
