User API
=========

`Bebo.User is` for getting user info.

Bebo.User.get
-----------------------------------

`Bebo.User.get(user, callback);`

The get() function will return data about a user or users depending on how it is called.

The user field can be passed as ‘me’ to retrieve your own data::

    Bebo.User.get('me', function(err, user){
        if(err){ 
            return console.log('error retrieving user', err) 
        }
        console.log('user', user); 
        // returns an object containing your user data
    });

The user field can also be passed as ‘all’ to retrieve data on all users in the server::

    Bebo.User.get('all', function(err, users){
        if(err){ 
            return console.log('error retrieving users', err) 
        }
        console.log('user', users); 
        // returns an array of objects contianing user data
    });

The user field can also be passed as an array of user ids to retrieve data on a specific set of users::

    Bebo.User.get(['0112358132134','4312318532110'], function(err, user){
        if(err){ 
            return console.log('error retrieving users', err) 
        }
        console.log('user', users); 
        // returns an array of objects contianing user data
    });

Bebo.User.update
------------------

`Bebo.User.update(user, callback);`

The update() function will update the users information in the database and return the result. User in an object containing the keys and values you want to update::

    Bebo.User.update(user, function(err, user){
        if(err){ 
            return console.log('error updating user', err) 
        }
        console.log('user', user); 
        // returns an object containing your user data after update
    });