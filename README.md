# yarsp

Yet Another React.js Starter-Pack 💎🛡 

## What is this project about ?

This is my own launcher-pack - it will evolve when I have time

## Choices

* The project uses **route.ts** to generate routes and access control.
* The project is using **Typescript** - "prop-type" library is not needed
* The project is using **useContext and useReduce** to manage application-level state - Redux is not needed in this project (another repo will implement it)
* The project is using **Sass** - it will probably be replaced / completed by css-in-js
* The project is using **Create-React-App scripts** - it will be removed in later versions
* The project is using **functions** to describe React's components - no classes are involved.

* NB: Do NOT rely on a front-strategy-only to grant access rights, your back **MUST** control it on each request.

## Guide

* Error pages (404, 403, Server unavailable) are handled out of the box
* The login/logout and session logic are there out of the box
* The routing logic is available out of the box
* A page layout is available out of the box
* A context is defined on the App level

## Run localy (dev mode)

* npm i
* npm run start

It will:
* Show "loading" for a second, the app is loading and session being set
* Show the public landing page
* if you go to /shared you'll see the shared page
* if you go to /action/accept/kzW4 you'll see the action page
* if you go to /private you will see a 403 error
* if you go to /anything you will see a 404 error
* From the login page, click on "login", you are logged in
* Click on "go to /page", you will access the route /page, forbidden before
* Click on "log out", you are logged out

**If I refresh the page I loose the session**

This is the expected behaviour. As all single pages applications, you get your session from the server. In this case there is no server to hold the session. If so, you would not be logged out.

## Notes

* There is no navbar,
* There are no animation, no style (appart from resetting all css and adding responsive breakpoints)
* Fetch have been replaced by setTimeout to mock a fetching, don't be surprised ...

## Build

* npm run build for local build

**About the .env:**    

The environment variables will be used only during the build of the app. You can check CRA documentation for a strategy using **.env.local**, **.env.production** ... 

## Deploy

The choice is yours:
* **AWS S3** Buckets paired with Route53 and CloudFront are very strong, easy and cheap to host a static website with low traffic. Start by droping the files, you'll build a deploy-and-rollback strategy when needed, with **CodeBuild** or other platforms as **buddy.io**.
* **Host it** on a server with or without Docker (AWS / Heroku / DigitalOcean allows both strategies)

## Good practises used

## TODO 
*[ ] Remove CRA  
*[ ] Add Docker for server hosting   
*[ ] Add tests    
 
