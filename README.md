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
