# Real-time-Java-project
step 1 - Cloned the java project from github using command "git clone <repo link>".
         
step 2 - Installed maven and build a source code using command "mvn verify". This will create executable war file which we have to deploy over tomcat webserver.
         
step 3 - A docker file is created which will pull tomcat image and deploy executable dile in desired location.
          
![image](https://user-images.githubusercontent.com/114205101/215757730-1f7157ae-b005-4f7e-8f1a-1b70a2e2350a.png)

       - There is an alternative which i tried  just for exprimentation i.e. i tried to pull ubuntu image and install apache tomcat in this container using docker file 
        
![image](https://user-images.githubusercontent.com/114205101/215758091-5e881af2-e13e-4982-b602-b690bd2ce189.png)

        
         
step 4 - A source code with executable war file and dockerfile is pushed to git hub.
         
step 5 - jenkins cluster is created with 3 servers one is master and other two are slaves (test & prod)

![image](https://user-images.githubusercontent.com/114205101/215759228-8f728fd4-f5fb-4acc-b7e3-8234cbd40a20.png)

step 6 - activating github-webhook integrate github with jenkins which will automate the pipeline

![image](https://user-images.githubusercontent.com/114205101/215760430-4426a299-ee97-45f3-8b2f-9292e8e905cf.png)
![image](https://user-images.githubusercontent.com/114205101/215760618-b8ea0173-2266-4ae9-8acc-24d734418129.png)



step 7 - creating new job in jenkins which will deploy application on test node, also commands to build docker image and run it are also included in executable shell in jenkins.

![image](https://user-images.githubusercontent.com/114205101/215762408-383d7b8d-cb30-4c54-80be-cd527335907f.png)

step 8 - After successfull completion of job 1 on test server it will deploy a website on sepcified port.

![image](https://user-images.githubusercontent.com/114205101/215762540-b4d755dc-b3fa-47bf-908b-61eb31bb95fe.png)


       This is how we can deploy a simple java project on single server. But our main objective is to make this application highly scalable, highly available and highly performant , hence we will integrate ansible and kubernetes in same project.



