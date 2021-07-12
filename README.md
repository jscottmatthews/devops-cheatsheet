# devops-cheatsheet

commonly used commands / CLI tricks for some of the more popular devops tools

<h3>Git</h3>

<h3>Docker</h3>

    docker build -t <user/image:tag> .
    docker run -d -p 8080:8080 <user/image:tag>
    docker logs <container>
    docker container pause <container>
    docker push <user/image:tag> 
    docker volume create volume_name
    docker exec -it <container name> /bin/bash

Dockerfile template
    
    FROM node:12

    WORDIR /app
    
    COPY package*.json ./
    
    RUN npm install 
    
    COPY . .
    
    ENV PORT=8080
    
    EXPOSE 8080
    
    CMD ["npm", "start" ]

</div>

<h3>Kubernetes / GKE</h3>
    kubectl get pods
    kubectl apply -f file.yaml
    kubectl port-forward <pod_name> <port:port>

<h3>Terraform</h3>

    wget https://releases.hashicorp.com/terraform/1.0.2/terraform_1.0.2_linux_amd64.zip
    unzip terraform_0.13.0_linux_amd64.zip 
    sudo mv terraform /usr/local/bin/
    terraform -v
    
    terraform init
    terraform validate
    terraform plan
    terraform apply
    terraform destroy
    
<h3>Ansible</h3>

    python -m pip install --user ansible
    pip install requests google-auth
    


<h3>Google Cloud Shell / SDK</h3>
GOOGLE_CLOUD_PROJECT is a present environmental variable containing project ID
    
    gcloud config set project <project>
    gcloud config list
    gcloud iam service-accounts list 
    gcloud iam service-accounts keys create key.json --iam-account <email_address>
    ssh-keygen -t rsa -b 1024 -N '' -f ~/.ssh/ssh_key
    export PROJECT_ID=$(gcloud config get-value project)    #set project ID as an environment variable 
    gcloud iam service-accounts list
    gcloud iam service-accounts keys create key.json --iam-account=<email_acct>
    
    gcloud container clusters get-credentials <cluster_name> --zone=<zone>

    
    gcloud container clusters create 
    


    

