Utilities API
============

`Bebo.Utils` is for accessing nice dev tools, such as figuring out which device your user is on.

Bebo.Utils.isMobile()
------------------

`Bebo.Utils.isMobile();`

The isMobile() function returns a boolean describing whether the user is on a mobile device (client or web) or on a computer (web)::

     if(Bebo.Utils.isMobile()){
     	//render mobile page
     } else {
     	//render desktop page
     };

Bebo.Utils.getImageUrl()
------------------

`Bebo.Utils.getImageUrl();`

The getImageUrl() function returns the base image url for the current Bebo platform::
	
	var user_id = //a Bebo user id
	var profile_pic = Bebo.Utils.getImageUrl() + "/image/user/" + user_id;

Bebo.Utils.getDevice()
------------------

`Bebo.Utils.getDevice();`

The getDevice() function returns either "ios", "android", or "web", depending on what device the user is on::
		
		var device = Bebo.Utils.getDevice();
		if (device == "ios"){
		  //User is on iOS native app!
		} else if (device == "android"){
		  //User is on Android native app!
		} else {
		  //User is on web (either mobile or desktop)
		};
