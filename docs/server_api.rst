Server API
==============

`Bebo.Server` is for getting server info.

Bebo.Server.getId
--------------------

`Bebo.Server.getId()`

Returns the Server’s ID::

    Bebo.Server.getId();

    >"54a371caeaa521fcb1da71ca69a467fd"

Bebo.Server.get
--------------------

`Bebo.Server.get(callback);`

Returns information about the current Server::

    Bebo.Server.get(function(err, server){
        if(err){ 
             return console.log('error getting roster', err) 
        }
        console.log('server', server); 
    });

Example Response::

    {
      "stream_id": "84a771caeaa541fcb1fa71ca69a467fc",
      "user_id": "8160ab72165343428d41774cd52013d5",
      "theme": "This is the name of theserver",
      "viewer_ids": [
        "8160ab72165d4dd28d41774cd52013d5"
      ],
      "creator": {
        "user_id": "8160ab72165343428d41774cd52013d5",
        "username": "myusername",
        "image_url": "https://a.imgdropt-dev.com/image/fc2a7a1b-3b83-422f-b800-15a73341e79e",
        "title": "this is the users bio",
        "updated_at": 1472252035752,
        "created_at": 1472251983723,
        "days_count": 22
      },
      "viewer_count": 1,
      "access_code": "123456",
      "flags": {
        "is_host": true,
        "is_creator": false
      },
      "unread_widgets": {
        "roster": 0,
        "furqan_dev": 0,
        "video-chat": 0,
        "sdk-test": 0,
        "hello-world": 0,
        "direct-message": 3,
        "camera": 0,
        "wall": 15,
        "create-room": 0
      },
      "unread": 18,
      "widgets": [
        {
          "widget_id": "wall",
          "title": "Discussions",
          "stream_id": "84a771caeaa541fcb1fa71ca69a467fc",
          "image_url": "https://a.imgdropt.com/image/3ff04ed6-eccf-4581-8211-69ed4db57a7a",
          "user_id": "8160ab72165343428d41774cd52013d5",
          "widget_url": "https://widgets.blab-dev.im/wall/9f0e2e819e1f2021c0344f734abe787041f93942/index.html",
          "updated_at": 1473385093281,
          "viewer_ids": [
            "8160ab72165343428d41774cd52013d5"
          ]
        }
      ],
      "updated_at": 1474071661934,
      "created_at": 1472461061940,
      "code": 200,
      "current_at": 1474071860007
    }

Bebo.Server.getRoster
-----------------------

`Bebo.Server.getRoster(callback)`

Returns Users in the server::

    Bebo.Server.getRoster(function(err, roster){
        if(err){ 
             return console.log('error getting roster', err) 
        }
        console.log(roster); 
    });

Example Response::

    [{
      "user_id": "a9ed30d820c54ec4b8c505c2e069c435",
      "username": "my_username",
      "image_url": "https://cf-i-02.bebo-img.com/user_profile_images/a9ed60d880c54ec4b7c505c2e069b435/8d9dc5dba3d7435ab53e2d3fd6abe0ec.png",
      "title": "This is the users bio",
      "updated_at": 1472161956533,
      "created_at": 1463740829193,
      "days_count": 120,
      "code": 200,
      "current_at": 1474072623938
    }]