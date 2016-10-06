Camera API
===============

`Bebo.Camera` is for accessing & capturing the native camera on an iOS or Android device.

Bebo.Camera.previewOn
---------------------

`Bebo.Camera.previewOn(side);`

The previewOn() function will trigger the native camera preview::

    Bebo.previewOn('front'); or Bebo.previewOn('back');

Bebo.Camera.previewOff
-------

`Bebo.Camera.previewOff();`

The previewOff() function will turn off the native camera preview::

    Bebo.previewOff();

Bebo.Camera.capturePhoto
---------------------
    
`Bebo.Camera.capturePhoto();`

The capture() function will capture a photo if the camera preview is open::

    Bebo.Camera.capturePhoto();