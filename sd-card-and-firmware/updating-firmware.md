# Firmware/Configuration

{% hint style="info" %}
Updating your firmware is important in order to obtain the latest features and bug fixes. The Duet Maestro board uses a fork of RepRap firmware to control a 3D printer. 
{% endhint %}

## Firmware:

The version of the Duet Firmware we are currently running is: **2.02RC2**

Here are the direct download links you will need to update your firmware as well as your Duet Web Control:

 [Duet Web Control](https://github.com/dc42/RepRapFirmware/releases/download/2.02RC2/DuetWebControl-1.22.3.zip)

[Firmware](https://github.com/dc42/RepRapFirmware/releases/download/2.02RC2/DuetMaestroFirmware.bin)

{% hint style="danger" %}
**Warning: Updating your firmware can cause unintended consequences. Be aware that upgrading or downgrading to unstable firmware versions can cause unexpected bugs and issues. Use caution!**
{% endhint %}

## Identifying Firmware Version

In order to find out if you want to update the firmware on the Duet Maestro you need to find your current version. You can view the RepRap firmware version in the Duet Web Console Settings Tab. Alternatively, you can use `M122`, command `M122` is the diagnose/debug command for RepRap firmware. If you send command `M122` the board will display a lot of debug statistics. In the first few lines the board will print out what firmware version it is running. Based on your firmware version, you might be able to identify if you are encountering a specific bug. Check DC42's github page regularly in order to read the latest firmware changes and see if any would be useful to you.

![Checking the RepRap Firmware Version](../.gitbook/assets/7f3tzsd7jhrwm9se-firmwareversionid.png)

## Upgrading System Firmware via the Duet Web Console

1. Download the desired firmware version from DC42's github page. This will be a _.bin_ or binary file called _**DuetMaestroFirmware.bin**_.
2. Download the ****_**iap4s.bin**_ file, this is necessary in order to update the firmware.
3. Go to the settings tab of the Duet Web Console and find the ****_**Upload File\(s\)**_ button. Note: this is not for uploading prints. Files uploaded here will be stored in the ****_**sys/**_ ****directory of the microSD card. Upload the _**iap4s.bin**_ and _**DuetMaestroFirmware.bin**_ files.

   ![aosmza6ID0m8KJ7A-uploadsysfiles.png](../.gitbook/assets/aosmza6id0m8kj7a-uploadsysfiles.png)

4. Once both files are uploaded successfully, go to the ****_**G-code Console**_. Send the command `M997 S0`. This will begin the process of upgrading Duet firmware.
5. When the firmware upgrade is completed, you can visit the _**Settings**_ ****tab in order to ensure that the _**Firmware Version**_ has been updated to the preferred version. 
6. If you prefer, you can now delete the _**iap4s.bin**_ and ****_**DuetMaestroFirmware.bin**_ files from the ****_**sys/**_ directory.

## Other Resources

1. [Duet 3D Wiki: Updating and Installing Firmware](https://duet3d.dozuki.com/Wiki/Installing_and_Updating_Firmware)
2. [Duet3D Forum](https://forum.duet3d.com/): For firmware and Duet specific questions
3. [Duet Fork of RepRap Firmware](https://github.com/dc42/RepRapFirmware)
