# A demo of development & production environments implemented via gcloud CLI

Transcript & slides are below.  Please click this demo video to hear it with sound.   
![demo](https://user-images.githubusercontent.com/38410965/111925621-0a688100-8a80-11eb-8087-4662b5a78992.mp4)

#

> **transcript for slide 7.1** *hello everyone thank you for watching this video that quickly demos using local terminal and git for app development and Google app engine for production.  and finally a trigger linkage between them for CICD.  we start with the basics: app, main, requirements, and make file.* 

### Development and Production Environments
Steve Depp MSDS 434 section 55 

Setup Continuous Delivery on GCP Platform with Google App Engine and Cloud Build.
(This implements via gcloud CLI the architecture demo'd via GCP console by Noah Gift [here](https://www.youtube.com/watch?v=_TfWdOvQXwU)).

**Development: Hello_world flask app with the usual suspects:**.  
- app.yaml
-	main.py
-	requirements.txt
-	Makefile

<img width="682" alt="dev-prod-demo" src="https://user-images.githubusercontent.com/38410965/112039665-a941bb80-8b1a-11eb-941c-7e5985e9c466.png">

<img width="682" alt="Backup File" src="https://user-images.githubusercontent.com/38410965/112039674-aba41580-8b1a-11eb-830b-4ef21b36cf20.png">

#

> **transcript for slide 7.2** *import dependencies.*

### Development: Hello_world flask app 

Import dependencies
—>	make install 

<img width="682" alt="dev-pred-denol" src="https://user-images.githubusercontent.com/38410965/112041502-d8f1c300-8b1c-11eb-862a-be0de7f211de.png">

#

> **transcript for slide 7.3** *test locally on a development server.  here we call **app create** before calling main.py with python but this could have gone in any order since app create still is a local development environment command.*   

### Development: Hello_world flask app 

Test locally with development server locally

<img width="682" alt="Successt The app is now created  Please use 'geloud app deploy' to deploy your" src="https://user-images.githubusercontent.com/38410965/112041695-11919c80-8b1d-11eb-89b4-f47fb2907db7.png">

<img width="686" alt="©127 0 0 18080" src="https://user-images.githubusercontent.com/38410965/112041704-148c8d00-8b1d-11eb-80bd-4953165a3da5.png">

#

> **transcript for slide 7.4** *we improve the code locally and re test.  we can see logs change here in light blue as we hit the end point.*     

### Development: Hello_world flask app 

Improve code and test locally

<img width="682" alt="an for a project is irreversible and" src="https://user-images.githubusercontent.com/38410965/112041872-4140a480-8b1d-11eb-9d59-c26bb29d15af.png">

<img width="686" alt="I like to make Al apps" src="https://user-images.githubusercontent.com/38410965/112041886-44d42b80-8b1d-11eb-9845-813b95693a6c.png">

#

> **transcript for slide 7.5** *deploy to production and hit the production server at Google.*   

### Deploy to Google Cloud - production 

<img width="682" alt="Services" src="https://user-images.githubusercontent.com/38410965/112042010-68977180-8b1d-11eb-9e0a-d75102240b9e.png">

<img width="860" alt="httpsdev-prod-demo uc r ap X" src="https://user-images.githubusercontent.com/38410965/112041993-646b5400-8b1d-11eb-810e-80602d2abada.png">

#

> **transcript for slide 7.6** *future development changes would be pushed to a development branch and then merged with master.  in this example any push from local terminal to GitHub master triggers a google app redeployment which is ...*   

### CICD   
Automating GitHub commits to GCP deploy   
= automatic production deployment

<img width="682" alt="dev-prod-demo" src="https://user-images.githubusercontent.com/38410965/112042134-8cf34e00-8b1d-11eb-9abb-f40c32ebc817.png">

#

> **transcript for slide 7.7** *... true cicd.  this is an example of that occurring, but ...*   

### CICD
Development environment stages in GitHub —> merges deploy to production end user automatically

<img width="682" alt="def bob()" src="https://user-images.githubusercontent.com/38410965/112042240-ae543a00-8b1d-11eb-839a-3b83f787e8c6.png">

<img width="675" alt="20201029001924" src="https://user-images.githubusercontent.com/38410965/112042252-b2805780-8b1d-11eb-836e-d9ad1bff6901.png">

#

> **transcript for slide 7.8** *... there was and still is a wrinkle with permissions.  thank you for watching.*

### Wrinkle:   
CICD permissioning needs ironing out.

<img width="1029" alt="Build details - Cloud Build - de" src="https://user-images.githubusercontent.com/38410965/112042394-d80d6100-8b1d-11eb-9f95-8065deb09460.png">
