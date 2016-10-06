Camera API
===============

`Bebo.Camera` is for accessing & capturing the native camera on an iOS or Android device.

Bebo.Camera.previewOn
---------------------

`Bebo.Camera.previewOn(side);`

The previewOn() function will trigger the native camera preview::

    Bebo.previewOn('front'); or Bebo.previewOn('back');

Bebo.Camera.previewOff
-------

`Bebo.Camera.previewOff();`

The previewOff() function will turn off the native camera preview::

    Bebo.previewOff();

Bebo.Camera.capturePhoto
---------------------
    
`Bebo.Camera.capturePhoto(callback);`

The capture() function will capture a photo if the camera preview is open::

    Bebo.Camera.capturePhoto(function(err,url){
    	if (err){
    		console.error(err);
    		return;
    	}
    	console.log(url); //<--- url is a url to your image.
    });
.. note:: Url is *only*  usable within the app. If you want to host/access this image elsewhere, use `Bebo.uploadImage <misc_api.html#bebo-uploadimage>`_ 