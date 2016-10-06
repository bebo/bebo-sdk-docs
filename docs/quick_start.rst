Quick Start
===============

Example 1: Fork existing room with Bebo SDK
#############

**Goal**:

    Fork and launch 'chat' **room** on Bebo, a basic messaging experience like iMessage or Slack:

#. Fork the 'chat' **room** at https://github.com/bebo-rooms/chat to your own https://github.com/<your-username>/<new-room-name> repo
#. :code:`$ git clone git@github.com:<your-username>/<room-name>.git` to clone your fork to your local machine
#. Follow its README.md instructions. They will look like :code:`npm setup` :code:`npm install` etc.
#. :code:`$ git checkout -b gh-pages` to create and switch to a new gh-pages branch
#. :code:`$ git push origin gh-pages` to tell GitHub to host your code at https://<your-username>.github.io/<room-name>
#. Verify it’s up at https://<your-username>.github.io/<room-name>
#. Open Bebo on your phone > tap gear icon > tap Add Room > enter https://<your-username>.github.io/<room-name>

BOOM! You have a **room** with fully functional chat.

.. image:: http://i.imgur.com/lLLu6i9.png
   :align: center
   :target: getting_started.html

Example 2: Fork empty room > add Bebo SDK
###############

**Goal**:

    Fork blank slate 'hello-world' **room** repo, and:

    A) get basic user information
    B) add push notification functionality
    C) store something in the Bebo database.

Now let's try adding in some actual Bebo SDK functionality to a new **room**.

#. Fork the 'hello-world' **room** at https://github.com/bebo-rooms/hello-world to your own https://github.com/<your-username>/<new-room-name> repo
#. :code:`$ git clone git@github.com:<your-username>/<room-name>.git` to clone your fork to your local machine
#. Follow its README.md instructions. They will look like :code:`npm setup` :code:`npm install` etc.
#. :code:`$ git checkout -b gh-pages` to create and switch to a new gh-pages branch
#. :code:`$ git push origin gh-pages` to tell GitHub to host your code at https://<your-username>.github.io/<room-name>
#. Verify it’s up at https://<your-username>.github.io/<room-name>
#. Open Bebo on your phone > tap gear icon > tap Add Room > enter https://<your-username>.github.io/<room-name>
#. Open index.html 

.. image:: http://i.imgur.com/lLLu6i9.png
   :align: center
   :target: getting_started.html

More examples
############

* For a full list of **rooms**, visit https://github.com/bebo-rooms
* Additional blog post walkthroughs of examples at :doc:`examples`

.. note:: We breezed over a ton of concepts here. If you're uncomfortable, read :doc:`/getting_started` instead.