Share API
============

`Bebo.Share` is for sharing and inviting friends to your group through social media. All these functions can also be done through `Bebo.openURI() <misc_api.html#bebo-openuri>`_, but the functions below will compile your message depending on which device the user is on (iOS/Android). Bebo will add "Here's the link to join: {{your server access code}}" at the end of your message.

.. warning :: Experimental, subject to change!

Bebo.Share.sms
------------------

`Bebo.Share.sms(string);`

The sms function will compile a text for the user's native SMS application (text messages).

::

		Bebo.Share.sms("Hey man check it!");

Bebo.Share.whatsapp
------------------

`Bebo.Share.whatsapp(string);`

The whatsapp function will compile a message for WhatsApp (if the user's phone has it installed).

::

		Bebo.Share.whatsapp("Yo I can send through WhatsApp too!");

Bebo.Share.twitter
------------------

`Bebo.Share.twitter(string);`

The twitter function will compile a tweet for Twitter (if the user's phone has it installed).

::

		Bebo.Share.twitter("Tweetin' for dayz through Bebo!1!1!1!");