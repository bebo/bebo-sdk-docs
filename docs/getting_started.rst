Getting Started
===============

Installation
---------------
Bebo SDK is a JavaScript library that enables deep functionality into the Bebo app. It allows you to create feature-rich **rooms** that can be added to your **group**. This allows you to create any **room** for you and your **group**.

Add Bebo SDK to your project — paste this snippet immediately after the :code:`<body>` tag in your index.html::

    <script>
      (function(_b,e,b,o){_b.Bebo={b:[],onReady:function(cb){this.b.push(cb)}}
        var s=e.createElement(b);s.type='text/javascript';s.async=1;s.src=o;
        var x=e.getElementsByTagName(b)[0];x.parentNode.insertBefore(s,x);})
      (window,document,'script','https://widgets.bebo.com/bebo.min.js');
    </script>

Usage
--------

The :code:`onReady` method is called when Bebo SDK has been loaded and initialized. This is very similar to the way the jQuery :code:`.ready()` function works.
The :code:`onReady()` function is typically used with an anonymous function::

    Bebo.onReady(function(){
        // Bebo is initialized
    });

.. important:: the :code:`onReady` function is required for all other functions to work.

Add Bebo SDK to a new or existing project
-----------------------------------

#. Join the Bebo Hackers group on Bebo (access code: :code:`wneseg`). Ask @furqan to provision you a new **room**. This will create a GitHub repo at https://github.com/bebo-rooms/<room-name>
#. :code:`$ git clone git@github.com:bebo-rooms/<room-name>.git` to clone the 'room-name' **room** to your local machine
#. :code:`$ mv chat <some-new-name>` to rename the repo to your idea's name
#. Follow its README.md instructions. They will look like :code:`npm setup` :code:`npm install` etc.
#. Verify it’s up at username.github.io/projectname
#. Open Bebo on your phone > tap Group Settings > find your **room** > tap Add Room