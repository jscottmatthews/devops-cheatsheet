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

<h3>Terraform</h3>

    wget https://releases.hashicorp.com/terraform/0.13.0/terraform_0.13.0_linux_amd64.zip
    unzip terraform_0.13.0_linux_amd64.zip 
    sudo mv terraform /usr/local/bin/
    terraform -v
    
    terraform init
    terraform plan
    terraform apply
    terraform destroy
    

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


    

