Notification API
==============================

`Bebo.Notification` is for sending notifications to users.

Bebo.Notification.users
----------------------------

`Bebo.Notification.users(title, body, users, callback);`

The users() function will notify the specific users you specify::

    var title = "some title";
    var body = "some body";
    var users = ["user_id1", "user_id2"];
    Bebo.Notification.users(title, body, users, function(err, resp){
        if(err){ 
           return console.log('error sending notification', err); 
        }
        console.log('resp', resp); // an object containing success
    });

Bebo.Notification.roster
----------------------------

`Bebo.Notification.roster(title, body, callback);`

The roster() function will notify all members of a server::

    var title = "some title";
    var body = "some body";
    Bebo.Notification.roster(title, body, function(err, resp){
        if(err){ 
            return console.log('error sending notification', err); 
        }
        console.log('resp', resp); // an object containing success
    });