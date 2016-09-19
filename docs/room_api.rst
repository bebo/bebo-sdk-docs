Room API
===============

`Bebo.Room` is for getting room info.

Bebo.Room.getId
------------------------

`Bebo.Room.getId();`

returns the unique id of the room::

    var room_id = Bebo.Room.getId();

Bebo.Room.emitEvent
------------------------

`Bebo.Room.emitEvent(data);`

Allows communication between clients. Data passed through this function will be received by all clients who are in the same room. This should be paired with the onEvent function below.

The data parameter should pass an object containing key value pairs you would like to pass between all clients::

    Bebo.Room.emitEvent({foo: "bar"});

Bebo.Room.onEvent
------------------------

`Bebo.Room.onEvent(callback);`

Receives communication between clients. Data passed through emitEvent will be received inside this callback::

    Bebo.Room.onEvent(function(data){
        console.log('data', data); 
    });
    > {foo: "bar"}

Bebo.Room.lastUsed
------------------------

`Bebo.Room.lastUsed(callback);`

Returns back a date (epoch) when the user last loaded your room::

    Bebo.Room.lastUsed(function(err, resp){
        if(err){ return console.log('error retreiving data', err) };
        console.log('resp', resp); // object containing last used timestamp
    });

Note: This will return a promise if no callback is passed.

Bebo.Room.uploadImage
------------------------

`Bebo.Room.uploadImage(file, callback);`

Allows image uploading to our server. Supports most common image formats. Note: file should be a non stripped base64 string::

    Bebo.Room.uploadImage(image, function(err, image){
        if(err){ return console.log('error uploading image', err) };
        console.log('image', image); // url to the image you uploaded
    });

Note: This will return a promise if no callback is passed.

Bebo.Room.onCallUpdate
------------------------

`Bebo.Room.onCallUpdate(callback);`

Returns a list of users that are currently called in and is triggered every time a change is detected::

    Bebo.Room.onCallUpdate(function(users){
        console.log('users', users); // an array of user objects
    });

Bebo.Room.onViewerUpdate
------------------------

`Bebo.Room.onViewerUpdate(callback);`

Returns a list of users that are currently called in the room. This is triggered whenever someone opens or closes the room::

    Bebo.Room.onCallUpdate(function(users){
        console.log('users', users); // an array of user objects
    });