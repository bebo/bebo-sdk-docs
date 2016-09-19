Getting Started
===============

Installation
---------------
BeboSDK is a JavaScript library that enables deep functionality into the Bebo App. It allows you to create feature rich applications that can be installed into your server. This allows you to create any room for you and your friends.

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

Call `Bebo.onReady(callback)`
##############################

The `onReady` method is called when the BeboSDK has been loaded and initialized. This is very similar to the way the jQuery `.ready()` function works.
The `onReady()` function is typically used with an anonymous function::

    Bebo.onReady(function(){
        // Bebo is initialized
    });

**IMPORTANT: the `onReady` function is required for all other functions to work.**