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
    terraform init
    terraform plan
    terraform apply
    

<h3>Google Cloud Shell / SDK</h3>

    gcloud config set project <project>
    gcloud config list
    

