---
title: Welcome
---

Welcome to first **Cicada PHP Framework** documentation. Cicada is light and simple PHP Framework aimed for creating **Back-End** application, although it can act as an API
serving data and delievering desiered content. The bigges flows of Cicada Framework is that is very light weight and it is adoptable to any kind of environment, it works prefectly on any platform with proper server. Talking about enivirnoment Cicada can be easly ported with apache virtual host as well as a main document root, on the other hand it also works good with nginx. In the core of Cicada is moduled Symfony HTTP request handler which is responsible for maniplating and distributing requests among controllers. Cicada have simple MVC structure which enables developers very neet and easly structured classes, simply there is no magic behind any of the classes every request and process is happening up front. So lets start with installation proccess. It is important to know that Cicada handles every request through index.php file, so every request have to go through it, which we will set during installation process

### Installation

For Cicada you got to have functional Apache or Nginx server for handling , mySql server for handling database, installed PHP and composer. 

### Setting the Environment

First we start with setting the VHosts on **Apache** creating and pointing host to root of our project (Explain further more process). Besides that it is requiered to set **.htacess** file which will overide every request which is not pointed to index.php since this is PHP Framework. In **.htacces** we are giving comand to apache to ignore every request to subfolders and to **Rewrite** pointing it to index.php where application begins it procces.

**nginx**


### Entry Point

After we are done with apache/nginx we are installing the reqierment for the framework the full package of framework you can download by simply requireing **composer reqire grobmeier/cicada** which will include our begining set. Next step is creating index.php file which is placed in main folder. In index.php we first reqire all dependencies for our framework by placing **<?php require "vendor/autoload.php";** now all our dependacies will be loaded and ready for use, index.php also represents the main routing points this framework over it we are building environment and necessary tools. Further more we need to create our source folder and to define it in **composer.json**, in section of autoload
we are placing **"psr-4"** component where we are defining namespace of our Application and the source folder. Right besides index.php we are creating **src** folder and in it we are creating new **Application.php** class. In Application we define all services that we will need but for now we are just setting the environment will be back to that. First step in Application.php we are placing same namespace that we defined in composer.json and extending our class with \Cicada\Application library which will deliever us all necesery accesories that we will need. Second we are creating empty constructor to be able to create an instance of it. Now we have Cicada library ready to run it we just need to create an instace of Application class in our index.php file. Right after **<?php require "vendor/autoload.php";** we are placing **use *namespace*\Application** to be able to create it.By creating instance **$app = new Application(); $app->run()** we have succesfully created our application so we can proced to next step. 

### Defining routes 

First step to routing is creating the Controllers, Controllers folder is created in **/src** folder **Controller** we start with creating **MainController.php** which will serve our first page. But before that we have to set namespace **namespace *namespace*\Controllers** "Controllers" will be the name of the folder where we setted our controllers. In controller we will have classic class structure with **__constructor(){}** and first method wich is end point of the route **public function index(){ return "It Works"}** to be able to use the routes we have to create an instance of the controller. Now in index.php file right after include Application, we are including controller **use *namespace*\Controller\MainController;** new step would be defining the instance of controller that will be used to create routes. **$mainController = new MainController();** now we have created instasances of $app and $mainController . To create a route we are defining it from $app which uses method that are inherited from \Cicada\Application we have a main elementary methods that are used defined by the standards, like 'post', 'get', 'delete', 'put'. In our case we will use the get we are defining route like **$app->get('/',[$mainController,'index'])** now our route is enabled and we can access to example.dev/ 












template from  [CloudCannon](http://cloudcannon.com/).
**Edition** is perfect for documenting your product, application or service.
It's populated with example content to give you some ideas.

ChatApp is a fictional chat application for sending messages and media to others.
Teams and friend groups would use ChatApp to stay up to date if it existed.

> [Sign up](http://example.com/signup) or learn more about ChatApp at [example.com](http://example.com/).

### Getting Started

Getting a message sent is quick and easy with ChatApp:

1. Sign up for an account
2. Add your friends from their email addresses
3. Type a message or send a photo

> Feel free to send us a message at [feedback@example.com](mailto:feedback@example.com) with your feedback.

### Features

Explore more of ChatApp by reading about our features:

#### Media

Send images, videos and other media to people. Sources include your computer, phone and Facebook.

#### Contact Syncing

Sync your contact list with your phone and/or Facebook contacts. Never lose your contacts between devices again!

#### Devices

This
