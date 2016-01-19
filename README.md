# Authentication
Here you can find sign-up page and sign-in page and integration with strompath using node.js

* The UI is developed by basic html and css(bootstrap). 
* Signup  and forgot password is include as modal(bootstrap modal)
* I had included google recaptcha for human verfication, will explain those things below in detail
* I had not included action classes for sign up, sign in, forgot password
* If we can include Angular here, we can reduce most of the work like verifying the input elements and it's authentication
* Once UI is done perfectly, I wil try to use strompath(for storing usernames and passwords). Strompath has an node API through which we can 
we can easily integrate. But strompath is not for free, you need to pay for them.
* Most of appliations these days are using passport library of node.js with bcrpt to store the login credentials, Doing that way
will make the login details application specific. Instead we can store them in cloud and use them for Mobile, tablet, Desktop applications


#### 1. Few CSS things, I thought of sharing
* To make the page more responsive, I had used **calc** funciton which will calcuate the space between top banner and bottom banner. This helps your page look more responsive eventhough the height of user screen changes. But if the user screen is so small, it's better to remove the left side contents and place the other contents of the page one below the other. Currently i did not implemented it perfectly, but you can use the bootstrap columns to do that easily.

```css
.sign-in-panel {
    height: -moz-calc(100% - 160px) !important;
    height: -webkit-calc(100% - 160px) !important;
    height: calc(100% - 160px) !important;
    background-color: #27303F;
}
```
* Most of the places I had used not used short hand notation, But the recomendation approach from experts is use **short hand notation**. Margin, border, padding, background, font, list-style, and even outline supports short hand notation.  

**for example:** 
``` css
p { margin-top: 10px;
	margin-right: 20px;
	margin-bottom:  30px;
	margin-left: 40px; }

	
	should be replaced with 

p { margin: 10px 20px 30px 40px; }
```

This will reduce the coding time, improves readability, loads less code on the browser,...
	
	
* I had wrote some rough documentation because the code is not that complex to understand, but writing documentation is always an recomended approach. Other will find it so useful and you can reduce the production time. 

* Since there is only one css file in this project I did not used any compressed tools for css. If there are more number of css files, then you need use some compress library to compress those css files into one file as it will reduce the no of requests from browser to server and saves the user bandwidth.

* Most of the work that you do using Javascript can be done with css especially by using css3. I would have missed and used javascript, But it's better if we use media queries or latest css3 features.
 
* Use less instead of using css, Because it reduces lots of code and increases the readability.

* since i had used less no of icons i did not clubbed them into an sprite image, Its better if you can club them into an sprite image as it will reduces the browser requests to the server and reduces the user bandwidth.

* finally, put the css at the top. remove unneceesery white spaces, organise the code. 


#### The output will be as follows

#####Sign In page
![alt tag](https://github.com/Zakir289/Authentication/blob/master/Authentication_images/signin.png)

##### Sign up page
![alt tag](https://github.com/Zakir289/Authentication/blob/master/Authentication_images/signup.png)

##### Forgot password page
![alt tag](https://github.com/Zakir289/Authentication/blob/master/Authentication_images/forgotpasswd.png)

##### Errors 
![alt tag](https://github.com/Zakir289/Authentication/blob/master/Authentication_images/forgotpasswd.png)
![alt tag](https://github.com/Zakir289/Authentication/blob/master/Authentication_images/error2.png)

####2. If you want to carousel images instead of grey background, then add the below code with your customized images

```html
<div id="myCarousel" class="carousel slide sign-in-carousel">
  <ol class="carousel-indicators">
    <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
    <li data-target="#myCarousel" data-slide-to="1"></li>
    <li data-target="#myCarousel" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="item active">
      <div class="fill" style="background-image:url('images/background1.png');"></div>
    </div>
    <div class="item">
      <div class="fill" style="background-image:url('images/background2.png');"></div>
    </div>
    <div class="item">
      <div class="fill" style="background-image:url('images/background3.png');"></div>
    </div>
  </div>
</div>
```

```javascript
 $('.carousel').carousel({
    interval: 4000 //changes the speed based on the requirement
  })
```


#### 3. How to integrate google recaptcha

* Here I had included previous version of captcha, Because the page design does not support the new version of captcha. We can customize the new version also, but don't know I was more fascinated towards the previous version of captcha
* writing about old version of captcha is of no use, I will write the steps for the new version of captcha
* Please go through the below steps

**1:** you need an api key which you will getting from https://www.google.com/recaptcha/admin#list. You need to login into your Google account and get the api key from this link. for testing in local host, you can use any api key but for production you need to register the key.

**2:** Once step 1 is done, you will two keys. **Site key** and **Secret key** 
 
 **site key** will be used to html code and **Secret key** is used between your site and Google.  Make sure you keep it secret. 
 
 **3:** You need a javascript snippet for include recaptcha into your site. you need to directly include the file link in your index.html or any file where you include the javascript files. 
 ```javascript
 <script src='https://www.google.com/recaptcha/api.js'></script>
 ```
 Google supports different languages also, but I am not going into it. 
 **4.** You need to add the form markup when ever you need to add captcha to your sign up page. 
 ```html
 <div class="g-recaptcha" data-sitekey="******"></div>
````
The above explanation is for the latest one, not the one which I had implemented in sign up page.
	



* I will write the backend code for this in a seperate repository. I will be using strompath for storing the **Authentication** details and node.js. Strompath officially provide node API for integration or you can do with REST API. 
I prefer node API because it is pretty cool.


