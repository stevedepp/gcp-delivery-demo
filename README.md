# dev-prod-demo
A demo of development production environments implemented via gcloud

(please click on the video below to hear sound)   
![demo](https://user-images.githubusercontent.com/38410965/111925621-0a688100-8a80-11eb-8087-4662b5a78992.mp4)


> **7.1** *hello everyone thank you for watching this video that quickly demos using local terminal and git for app development and Google app engine for production.  and finally a trigger linkage between them for CICD.  we start with the basics: app, main, requirements, and make file.* 

### Development and Production Environments
Steve Depp MSDS 434 section 55 

Setup Continuous Delivery on GCP Platform with Google App Engine and Cloud Build
(this implements via gcloud the architecture demo'd via GCP console by Noah Gift [here](https://www.youtube.com/watch?v=_TfWdOvQXwU)

**Development: Hello_world flask app with the usual suspects:**.  
- app.yaml
-	main.py
-	requirements.txt
-	Makefile

<img width="682" alt="dev-prod-demo" src="https://user-images.githubusercontent.com/38410965/112039665-a941bb80-8b1a-11eb-941c-7e5985e9c466.png">

<img width="682" alt="Backup File" src="https://user-images.githubusercontent.com/38410965/112039674-aba41580-8b1a-11eb-830b-4ef21b36cf20.png">

   

- **slide 1:** import dependencies.  
- **slide 2:** test locally on a development server.  here we call **app create** before calling main.py with python but this could have gone in any order since app create still is a local development environment command.   
- **slide 3:** we improve the code locally and re test.  we can see logs change here in light blue as we hit the end point.     
- **slide 4:** deploy to production and hit the production server at Google.  
- **slide 5:** future development changes would be pushed to a development branch and then merged with master.  in this example any push from local terminal to GitHub master triggers a google app redeployment which is ...   
- **slide 7:** ... true cicd.  this is an example of that occurring, but ...   
- **slide 8:** ... there was and still is a wrinkle with permissions.  thank you for watching.
