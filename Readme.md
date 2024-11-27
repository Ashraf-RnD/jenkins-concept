# Jenkins Learning

### **Jenkins setup in docker**

#### Run Command
```shell
docker run -p 8080:8080 -p 50000:50000 -d -v /Users/alam.ashraful/Desktop/ashraf-RnD/jenkins-concept/jenkins_compose/jenkins_configuration:/var/jenkins_home jenkins/jenkins:lts
```
Expose port 8080 => default port ```-p 8080:8080```

Expose port 50000 => Master/Slave communication ```-p 50000:50000```

Run in detached mode => run container in background ```-d```

Bind named volume => persist data of jenkins ```jenkins_home:/var/jenkins_home```

---
Once the Container is created, check the logs 
```shell
docker ps -a

docker logs <container_id>
```
Get installation Password using
```shell
docker exec <container_id> cat /var/jenkins_home/secrets/initialAdminPassword
```
Save the installation password. For this instance 
```03836b98d01344d6ac8c6c5e66a2518c```

Check in the browser with URL: ```localhost:8080``` and use the previously got password 

---
