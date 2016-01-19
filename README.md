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


#### Few CSS things, I thought of sharing
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


	
	
