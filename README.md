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
