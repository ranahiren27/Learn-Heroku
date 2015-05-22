![](https://s3.amazonaws.com/kinlane-productions/api-evangelist/heroku/heroku-logo.png)

##Learn how to host your app on Heroku

###What is it?

Heroku is a cloud service that hosts your app. You can do this for free if you have a small app. 

###How?

You can deply your app using the Heroku GUI but that's not cool. We're gonna deploy command line style!

![](http://s2.quickmeme.com/img/14/14bd39c02c40e7e10a50a68aa2c385359b5097214a97fe131e88d21bf7996198.jpg)

---

Say you've been working on a project all week and you decide to deploy on Friday afternoon. Don't! Sometimes things go smoothly but sometimes and specially if it's your first time, this doesn't happen. Leave enough time for it just in case.

1. Please sign up on Heroku if you haven't already, they are more likely to let you use their service if you do. 


2. Once you've done that, please come back and run the following commands in your terminal:

```
heroku login
cd into your project
heroku create
```
The last command on that list will will give your app a random name, thus url but you can change this later if you want to. Alternatively you could do the following:

Click on the plus sign on the top right hand corner to create a new app:

![](https://raw.githubusercontent.com/Neats29/Learn-Heroku/master/add-new-app.png)

Select Europe if you're there and voilla!

![](https://raw.githubusercontent.com/Neats29/Learn-Heroku/master/app-name.png)


Ok back to the command line. Now you need to connect your project to this newly created 'app' on Heroku.

```
heroku git:remote -a whatever-you-like
```
And to deploy, checkout to the master branch and run:
```
git push heroku master
```

> That was so easy, why did you tell me not to do it on Friday afternoon?

'coz there's more...

#Environmental Variables

The above is fine if you don't have a database, user authentication or are not using any APIs that require tokens and passwords. But then again why won't you use Github pages if that's all you have. It's when you have to deal with credentials (and thus hiding them) that you have to turn to services like Heroku.

We need to hide our passwords, tokens, secrets etc and ensure that we don't push them to Github but the hosting service would needs them in order to run your app. This is where environmental variables come into place.










