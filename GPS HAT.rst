*********************************************
How to Build a Raspberry Pi Based Sensorgnome
*********************************************

.. image:: images/GPS-HAT_finished.jpg
  :alt: A finished GPS HAT, ready to be deployed.

Introduction
============
SensorGnomes are an essential component of the `Motus Wildlife Tracking System <https://motus.org/>`_. These devices act as radio receivers in a world-wide network, listening to radio transmitters that have been deployed on birds, bats, and insects by researchers trying to answer questions about movements on multiple scales.

The SensorGnome was originally designed at the Phil Taylor Lab at Acadia University and is now available for sale by `Compudata <https://compudata.ca/sensorgnome/>`_ and `RFS Scientific <https://www.rfsscientific.com/>`_.

Here I explain how to build one of these devices yourself.

See `Sensorgnome.org <https://sensorgnome.org/>`_ for more information.

Building a Sensorgnome
======================

Supplies
--------
 * Raspberry Pi Model B v1.2
 * Raspberry Pi Case
 * GPS HAT
 * 40-pin header
 * CR 1220 battery
 * uFL to SMA Adaptor
 * GPS Antenna
 * Micro SD Card and Reader - minimum of 16 GB recommended
 * Laptop
 * USB Power Adaptor with Micro USB
 * Waterproof Momentary Pushbutton Switch with LED
 * Socket for Pushbutton

Tools
-----
 * Soldering iron
 * Solder
 * Flux
 * Solder wick and/or solder sucker to clean up any mistakes
 * Hot glue gun + hot glue

Step 1: Solder 40-pin Header to GPS HAT
---------------------------------------

.. image:: images/gps_hat_unsoldered.jpg
  :alt: GPS HAT, ready to have the header soldered to it.

GPS HAT purchased from Adafruit typically comes with a 40-pin header that must be soldered to the board.

Instructions on soldering will not be described here.

Step 2: Soldering Pushbutton to GPS HAT
---------------------------------------

.. image:: images/pushbutton_unsoldered.jpg
  :alt: GPS HAT, ready to have the pushbutton soldered to it.

Pushbutton comes with multiple pins – see the specifications for your button to identify each terminal. Plug the pushbutton socket into the pushbutton so you know which wire corresponds with each pin.

Pins are soldered to the GPS HAT in the following order:

#. Netagive and common switch terminals to ground
#. Positive to GPIO#17
#. Normally Open to GPIO#18

Solder the wires of the Pushbutton Socket through the topside of the boards so that the wires come out of the topside.

.. image:: images/pushbutton_soldered.jpg
  :alt: GPS HAT, with the pushbutton soldered to it.

Double-check you are soldering the wires to the board in the correct order before you start soldering. There may be one wire left unused - you can leave it loose.

Instructions on how to solder will not be outlined here.

+--------------+-----------------+---------+
| Button Symbol| Button Terminal | GPS HAT |
+==============+=================+=========+
| \-           | Negative        | Ground  |
+--------------+-----------------+---------+
| C1           | Common Switch   | Ground  |
+--------------+-----------------+---------+
| \+           | Positive        | GPIO#17 |
+--------------+-----------------+---------+
| NO1          | Normally Open   | GPIO#18 |
+--------------+-----------------+---------+

Step 3: Assembling GPS HAT
--------------------------

.. image:: images/gps_hat_assembled.jpg
  :alt: GPS HAT, ready to have the pushbutton soldered to it.

Plug the uFL end of the uFL-to-SMA connector onto the uFL port on the GPS HAT, located adjacent to the square GPS Module and battery slot.

Use a hot glue gun to help fix the uFL connector to the board.

Insert the CR1220 battery into the battery slot, positive (flat) side up.

Step 4: Assembling Raspberry Pi
-------------------------------

.. image:: images/finished_sg.jpg
  :alt: A finished Sensorgnome.

Plug the GPS HAT on to the Raspberry Pi board using the 40-pin
header.

Install the Raspberry Pi + GPS HAT in the Raspberry Pi Case.
