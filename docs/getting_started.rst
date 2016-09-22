Getting Started
===============

Download Bebo App
---------------
1. Download `Bebo for iOS <https://itunes.apple.com/us/app/bebo-private-server-for-your/id943549087?mt=8>`_ or `Bebo for Android <https://play.google.com/store/apps/details?id=com.bebo.varys>`_ and create your own private group

.. note:: A group is a private space composed of members and rooms.

2. Every group has an access code that you can give to anyone (only people who have this code will be able to join)

.. note:: Your group is pre-loaded with a couple default rooms. You can add/remove any room. Rooms are websites that can do special things within Bebo.

3. Most Rooms are open source, available `on our GitHub <https://github.com/bebo-rooms>`_.

.. tip:: When you add a room, put in the name of the repo (example: `wall`) or any website.

4. Use Bebo SDK to add functionality to any website. Bebo SDK lets you create real time events, notifications, Database storage, etc. Anything you would need to create a fun social experience. Along with Audio, video (WebRTC) capabilities. All for free.

.. note:: Yes, this means you can create your own community, the way you want it. Your community may have different needs than others. If you prefer live streaming, add the video lounge. Create your own Gaming forum with discussions. Or build a place for friends to discuss politics. There’s no cost for this group, and theres no limit to what you can do.

Install Bebo SDK
---------------
Bebo SDK is a JavaScript library that enables deep functionality into the Bebo App. It allows you to create feature rich applications that can be installed into your server. This allows you to create any room for you and your friends.

How to add it to your project:

Load Bebo SDK
################

Copy-paste this snippet it right inside your <body> tag of your index.html::

    <script>
      (function(_b,e,b,o){_b.Bebo={b:[],onReady:function(cb){this.b.push(cb)}}
        var s=e.createElement(b);s.type='text/javascript';s.async=1;s.src=o;
        var x=e.getElementsByTagName(b)[0];x.parentNode.insertBefore(s,x);})
      (window,document,'script','https://widgets.bebo.com/bebo.min.js');
    </script>

Using Bebo SDK
--------

Call `Bebo.onReady(callback)`
##############################

The `onReady` method is called when Bebo SDK has been loaded and initialized. This is very similar to the way the jQuery `.ready()` function works.
The `onReady()` function is typically used with an anonymous function::

    Bebo.onReady(function(){
        // Bebo is initialized
    });

**IMPORTANT: the `onReady` function is required for all other functions to work.**