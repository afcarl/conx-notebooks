# Running Conx in VirtualBox

These are the steps required to download and run Conx in a VirtualBox image.

This option will allow you to run an entire Ubuntu operating system with all of Conx installed and ready to run. 

* VirtualBox Program size: 174 MB
* Ubuntu with Conx Compressed Image size: 3.9 GB (can be deleted after uncompressing)
* Ubuntu with Conx Uncompressed Image size: 9 GB

1. **Install VirtualBox**. Go to https://www.virtualbox.org, click on the giant
blue "Download VirtualBox 5.2" button, and choose the appropriate download link
for your system, or just click directly on one of the links below:

**Mac**:
- https://download.virtualbox.org/virtualbox/5.2.6/VirtualBox-5.2.6-120293-OSX.dmg

**Linux**:
- https://www.virtualbox.org/wiki/Linux_Downloads

**Windows**:
- https://download.virtualbox.org/virtualbox/5.2.6/VirtualBox-5.2.6-120293-Win.exe

Note: VirtualBox for Windows requires at least Windows 10 Professional, among other versions of Windows. 

2. **Download the Appliance**. After installing VirtualBox, download the file `virtualbox-conx-3.6.0.ova`
from the link below. This file is about 3.9G, so it may take some time to
download. You can save it anywhere you like on your system.

http://science.slc.edu/jmarshall/virtualbox-conx-3.6.0.ova

3. **Import Appliance**. Start VirtualBox, then choose `File` -> `Import Appliance` and select the
`virtualbox-conx-3.6.0.ova` file that you downloaded. Click Continue, then Import
(leave the default appliance settings as they are). This step may take a few
minutes to complete.

Note: You may have to increase your video memory for the Conx image to at least 32 MB to see the screen properly.

4. **Start the Virtual Machine**. In the VirtualBox side panel at the left, you should now see the virtual
machine "Conx 3.6.0 (Powered Off)". Double click on the machine to start the
boot process. After a minute or two, you should see the Ubuntu desktop.

5. **Start Jupyter**. Open a Terminal window by clicking on the Terminal icon in the upper left
corner of the screen. Type the command "jupyter notebook". This should bring up
a Firefox browser window running Jupyter.

6. **Test Conx**. In the upper right corner of the browser, choose New -> Python 3 to start a
new Python 3 notebook running. Then type:

```
import conx as cx
```

and press Shift-RETURN. You should see the message:

```
Using TensorFlow backend.
Conx, version 3.6.0
```

7. **Shutdown**. If this works, you're done! You can shut down the notebook by
selecting `File` -> `Close and Halt`. You can shut down the Ubuntu Virtual Machine by clicking
on the power button in the upper right corner of the Desktop and choosing `Shutdown`. You 
can then close VirtualBox.

8. **Cleanup**. (optional) You can now safely delete the file `virtualbox-conx-3.6.0.ova` from
your system.

9. **Regular Use**. To use VirtualBox regularly, go to step #4.

If you can't get VirtualBox to work, then you may want to try the Docker option,
or ask for help on the `conx-users` mailing list:

https://groups.google.com/forum/#!forum/conx-users

