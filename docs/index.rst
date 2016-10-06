.. Bebo Rooms documentation master file, created by
   sphinx-quickstart on Mon Sep 19 13:26:55 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Bebo SDK
======================================

Developers use Bebo SDK to build **rooms** for Bebo **groups**, and the Bebo community as a whole. Anyone with experience making a website can make a **room**.

**Rooms** are not webhooks. Or bots. They are full websites that can use Bebo SDK to: create real-time events, push notifications, database storage, user management, A/V (WebRTC). Anything you would need to create a fun social experience.

* A **group** is a private space composed of **people** and **rooms**.
* **Groups** are pre-loaded with default **rooms**. Any **group** can add/remove any **room**. 
* **Rooms** are websites that can do special things within Bebo, by tapping into **Bebo SDK**.
* Every **group** has an **access code** that you can give to anyone. Only people who have this code will be able to join.
* Most **rooms** are open source, available `on our GitHub <https://github.com/bebo-rooms>`_. All **rooms** are sandboxed. **Rooms** look like:

.. figure:: https://cdn-images-1.medium.com/max/600/1*X9DFiUH8R0OtZ34StE5p7Q.gif
   :align: center
   :alt: Rooms on Bebo

   Your group may have different needs than others. Prefer live streaming? Add the Video Lounge **room**. Prefer politics chat? Add the Chat **room**. There's no limit to what you can do.

.. image:: http://i.imgur.com/2zHJJGl.png
   :align: center
   :target: quick_start.html

Download Bebo
---------------
Download `Bebo for iOS <https://itunes.apple.com/us/app/bebo-private-server-for-your/id943549087?mt=8>`_ or `Bebo for Android <https://play.google.com/store/apps/details?id=com.bebo.varys>`_ and create your own private group

.. toctree::
   :maxdepth: 2
   :caption: Bebo SDK Documentation

   introduction
   quick_start
   getting_started
   examples
   

.. toctree::
   :maxdepth: 2
   :caption: API Methods

   api_methods
   user_api
   room_api
   server_api
   database_api
   notification_api
   camera_api
   audio_api
   misc_api

.. toctree::
   :maxdepth: 2
   :caption: Modules

   react_lib
   leaderboard



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

