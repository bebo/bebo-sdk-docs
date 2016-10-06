Misc API Functions
====================

Bebo.getRoster
------------------

`Bebo.getRoster(callback);`

The getRoster() function return a list of users that are members of your server::

    Bebo.getRoster(function(err, resp){
        if(err){ return console.log('error getting roster', err) };
        console.log('resp', resp); // an object containing users
    });


Bebo.onCallUpdate
------------------

`Bebo.onCallUpdate(callback);`

The onCallUpdate() function return a list of users that are currently called in. This would be triggered by callinand hangup above::

    Bebo.onCallUpdate(function(users){
        console.log('users', users); // an array of user objects
    });

Bebo.uploadImage
------------------

`Bebo.uploadImage(file, callback);`

The uploadImage() function allows you to send an image to our image hosting server. Supports most common image formats. Note: file should be a non stripped base64 string::

    Bebo.uploadImage(image, function(err, image){
        if(err){ return console.log('error uploading image', err) };
        console.log('image', image); // url to the image you uploaded
    });

Bebo.getWidgetId
------------------

`Bebo.getWidgetId();`

The getWidgetId() function returns the current widget id::

    var widget_id = Bebo.getWidgetId();

Bebo.getStreamId
------------------

`Bebo.getStreamId();`

The getStreamId() function returns the current stream id::

    var stream_id = Bebo.getStreamId();

Bebo.getEnv
------------------

`Bebo.getEnv();`

The getEnv() function returns the current environment (ios, android or local)::

    var env = Bebo.getEnv();


Bebo.lastUsed
------------------

`Bebo.lastUsed();`

The lastUsed() function returns back the last time the user used your app::

    Bebo.lastUsed(function(err, resp){
        if(err){ return console.log('error retreiving data', err) };
        console.log('resp', resp); // object containing last used timestamp
    });

Bebo.getStream
------------------

`Bebo.getStream(callback);`

The getStream() function is self explanatory for us but will be broken down into more getters for 3rd party devs::

    Bebo.getStream(function(err, stream){
        if(err){ 
            return console.log('error retreiving stream', err) 
        }
        console.log('stream', stream); 
        // returns a stream object
    });

Bebo.openURI
------------------

`Bebo.openURI(uri)`

The openURI() function will open the passed in URI. This is helpful for sharing, such as to Facebook, Twitter, through What's App, or even through your native SMS client. **NOTE: iOS and Android treat SMS URI's differently, do your research**:

        $("#twitter").on("click",function(){
            Bebo.openURI("https://twitter.com/intent/tweet?status=Hello")
        });
