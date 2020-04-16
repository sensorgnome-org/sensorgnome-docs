*******************************************************************
CTT Dongle - How to Update your Sensorgnome Software (Raspberry Pi)
*******************************************************************

.. image:: images/finished_sg.jpg
  :alt: A finished Sensorgnome, ready to be deployed.

Introduction
============

`Cellular Tracking Technologies <https://celltracktech.com/>`_ (CTT) has developed tags which operate on a different frequency (434 MHz) from Lotek's tags (~166.380 MHz). CTT has their own radio dongles which are effective and cheaper than FUNcube dongles (FCD), but they require a software patch for them to work on a Sensorgnome. These instructions are how to install this patch.


Supplies
======================
 * Assembled Raspberry Pi with SD card, button, and power adapter.
 * CTT Motus Adapter.

Steps for updating file to Sensorgnome
---------------------------------------

#. Download the CTT update from `here <https://s3.amazonaws.com/media.celltracktech.com/sensorgnome/raspberry/2019-11-12-rpi_ctt_dongle.tar.bz2>`__.
#. Rename the file to "sensorgnome_update.tar.bz2".
#. Connect to the Sensorgnome using :ref:`Wi-Fi <sg_build_step6>` or :ref:`Ethernet cable <sg_build_step7>`.
#. Install the FileZilla Client, available from the `project's website <https://filezilla-project.org/download.php?type=client>`__.
#. Open FileZilla and connect to the file system using the following credentials:
    * **Host**: sftp://192.168.7.2
    * **Username**: root
    * **Password**: root
#. Navigate to ``/boot/uboot/`` and upload the update file there.
#. Reboot the Sensorgnome and connect to it again.
#. If the CTT dongle still doesn't show up on the web interface, try rebooting again.
