************************************************
How to Change the Wi-Fi Settings on Raspberry Pi
************************************************

.. image:: images/finished_sg.jpg
	:alt: A finished Sensorgnome, ready to be deployed.
	:height: 300px
	:align: center

.. _introduction:

Introduction
============
SensorGnomes are an essential component of the `Motus Wildlife Tracking System <https://motus.org/>`_. These devices act as radio receivers in a world-wide network, listening to radio transmitters that have been deployed on birds, bats, and insects by researchers trying to answer questions about movements on multiple scales.

The SensorGnome was originally designed at the Phil Taylor Lab at Acadia University and is now available for sale by `Compudata <https://compudata.ca/sensorgnome/>`_ and `RFS Scientific <https://www.rfsscientific.com/>`_.

See `Sensorgnome.org <https://sensorgnome.org/>`_ for more information.

**Contents:**

* `Connecting - OPTION 1: Wi-Fi <#connecting-wifi>`_
* `Connecting - OPTION 2: Ethernet Cable <#connecting-ethernet>`_
* `Change Wi-Fi Settings - OPTION 1: Laptop <#change-wifi-laptop>`_
* `Change Wi-Fi Settings - OPTION 2: Android Smart Phone<#change-wifi-android>`_


`- Back to Top - <#>`_

.. _connecting-wifi:

Connecting - OPTION 1: **Wi-Fi**
-----------------------------------------------------------


.. youtube:: d0x9dIOvAr4

1. With the computer booted up, double-press the *Pushbutton* switch to activate the **Wi-Fi**.

2. Once active, the *Pushbutton* should blink slowly at a rate of 0.5 seconds on and 0.5 seconds off.

3. Using a *phone or laptop*, look for a Wi-Fi network with a name such as **"SG-###RPI3###"**, where '#' can be any letter or number.

4. Connect to the network using the same name of network as the password.

5. Once connected, open your web browser and navigate to the following address: 192.168.7.2

6. You should see a web page that says *'I am your SensorGnome'* with a bunch of live information about the device. A full description of the webpage will be described later. For now, the fact this page is loading will inform you that the Sensorgnome software has correctly been installed and that you have successfully connected to it.

`- Back to Top - <#>`_

.. _connecting-ethernet:

Connecting - OPTION 2: **Ethernet Cable**
-----------------------------------------------

1. With the computer booted up booted up, insert the *Ethernet Cable*.
cable into the *Raspberry Pi's* **Ethernet** port and your **laptop**.

2. Once connected, open your web browser and navigate to the following address: **sgpi.local**

3. You should see a web page that says **'I am your SensorGnome'** with a bunch of live information about the device.

4. If you are having trouble connecting, try the previous step with Wi-Fi.

`- Back to Top - <#>`_

.. _change-wifi-laptop:

Change Wi-Fi Settings - OPTION 1: **Laptop**
--------------------------------------------------

.. image:: images/FileZilla_01.png
	:height: 300px
	:align: center

#. Download FileZilla from their website:
#. Install the program with its default settings
#. Open the program and in the top bar you will see four text fields labelled Host, Username, Password, and Port.

#. In the 'Host' field, enter the address "sftp://192.168.7.2" if you are connected via Wi-Fi. If you are connected by an Ethernet cable, enter the address "sftp://sgpi.local".

..images:: images/network-txt_screencap_raw.png
	:height: 300px
	:align: center

#. For the username enter "root" and for the password enter "root" as well. The port field should be left blank.

#. Click the 'Quickconnect' button and you should see the following progress text in the Status frame.

#. The folders visible on the left-hand side of the window are on your laptop ('Local Site') – we will call this sections frame 1. After clicking the 'Quickconnect' button, you should also see folders appear in two frames located on the right-hand side of the window – this is the internal storage of your SensorGnome ('Remote Site'). We will call the top and bottom sections frame 2 and frame 3, respectively.

#. To navigate through your SensorGnome's storage, you can use either of frames 2 or 3 but note only frame 3 shows files (frame 2 is for navigation only!).

#. Navigate to the 'root' of the Sensorgnome, either by clicking on the folder '/' in frame 2 or by clicking the '..' folder in frame 3 until you can no longer navigate further.

#. From this location, navigate to the following folder: “boot” / “uboot”.

#. In here you can find a file called 'network.txt'. Right click on it and select 'view/edit'.

#. This file contains all the instructions required to enter the Wi-Fi settings. Once completed, save and close the file.

#. To make the changes come into effect, you will need to reboot your SensorGnome.

#. Once rebooted, review that your SensorGnome has been connected successfully by searching for its serial number in the list of receivers found on http://sensorgnome.org/status.


`- Back to Top - <#>`_

.. _change-wifi-android:

Change Wi-Fi Settings - OPTION 2: **Android Smartphone**
--------------------------------------------------------

1. Download and install **ES File Explorer** from the Google Play Store.

2. Open the program and open the top-left menu.

.. image:: images/Wi-Fi_android_step-01.jpg
	:height: 300px
	:align: center

3. Select **Network** and then **FTP**.

.. image:: images/Wi-Fi_android_step-02.jpg
	:height: 300px
	:align: center
.. image:: images/Wi-Fi_android_step-03.jpg
	:height: 300px
	:align: center

4. Open the folder '**192.168.7.2**' 

 * If prompted for a username and password, enter '**root**' for both.

.. image:: images/Wi-Fi_android_step-04.jpg
	:height: 300px
	:align: center

5. Scroll down until you see the '**boot**' folder and open it.

.. image:: images/Wi-Fi_android_step-06.jpg

6. Open the '**uboot**' folder and then open the file named '**network.txt**'.

.. image:: images/Wi-Fi_android_step-07.jpg
	:height: 300px
	:align: center
.. image:: images/Wi-Fi_android_step-08.jpg
	:height: 300px
	:align: center

7. Open the menu on the **top-right** corner and select **Edit**.

.. image:: images/Wi-Fi_android_step-09.jpg
	:height: 300px
	:align: center
.. image:: images/Wi-Fi_android_step-10.jpg
	:height: 300px
	:align: center

8. Read the instructions and edit the three lines of text as indicated.

.. image:: images/Wi-Fi_android_step-11.jpg
	:height: 300px
	:align: center

9. When all the correct information has beeen entered, press the back arrow on the top-left corner and confirm your edits.

.. image:: images/Wi-Fi_android_step-12.jpg
	:height: 300px
	:align: center

10. To make the changes come into effect, you will need to reboot your SensorGnome.

11. Once rebooted, review that your SensorGnome has been connected successfully by searching for its serial number in the list of receivers found on http://sensorgnome.org/status.


`- Back to Top - <#>`_