# CI/CD Process

Process Flow :- 

1) Jenkins job will pull the pipeline code from GITHUB and start the building process 
2) Jenkins will pull the source code from SCM (GITHUB) and store it in Jenkins workspace
3) Maven will kick off the JUNIT Test and the source code will be pushed to Sonarqube for static code analysis
4) Package the code into war file and push the code to Nexus Repository 
5) Ansible will pull the latest package from Nexus  and deploy it in Tomcat Server
