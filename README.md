ReplicatorG64bit
================

The needed files to convert ReplicatorG to run on a 64bit Java VM

I created this project so that it is easy to upgrade makerbot/ReplicatorG to run on a 64bit Java VM.  I kept the directory structure the same as ReplicatorG.  The directory name replicatorg-0040 will ofcourse be out of date when makerbot/ReplicatorG is upgraded

Please follow these steps to upgrade:
Check out this git project.
Rename rxtxSerial.dll to "rxtxSerial.dll 32bit" and j3dcore-ogl.dll to "j3dcore-ogl.dll 32bit".
Copy rxtxSerial.dll and j3dcore-ogl.dll from the git project to replicatorg-0040.
Change directory to lib.
Rename j3dcore.jar, j3dutils.jar, RXTXcomm.jar and vecmath.jar.  Add 32bit after the extension on each file.
Copy j3dcore.jar, j3dutils.jar, RXTXcomm.jar and vecmath.jar to the lib of your makerbot/ReplicatorG.

Change directory back to replicatorg-0040.
Make sure a 64bit Java is on the path.
Run ReplicatorG.bat.
The bat file has been configured to start off using 1GB of memory up to a maximum of 4GB.