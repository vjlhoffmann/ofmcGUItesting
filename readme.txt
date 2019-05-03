# Readme for ofmcGUI test users 05.04.2019

Please note that some features are still in development and might have known and unknown errors.

To be able to run the GUI you have to have Haskell platform installed, Java 12 installed and download the JavaFX 12 SDK
Links to download:

Haskell:
https://www.haskell.org/platform/
JavaFX 12:
Windows
http://gluonhq.com/download/javafx-12-0-1-sdk-windows/ 
Mac OSX
http://gluonhq.com/download/javafx-12-0-1-sdk-mac

Java 12:
https://www.oracle.com/technetwork/java/javase/downloads/jdk12-downloads-5295953.html

After installing Java 12 you need to unzip the JavaFX SDK folder where you like. I prefer the Java home folder.

Now you need to set a few Environment variables:

Guide for Windows:
1.  Open Control Panel -> System
2.  Click the "Advanced" tab
3.  Open "Environment Variables"
4.  Click on the "New" button under "System Variables"
5.  Add the following:
      Variable name: JAVA_HOME
      Variable value: C:\Program Files\Java\jdk-12.0.1 (or where java is installed on your computer)
6.  Click "Ok"
7.  Now select "Path" in the "System variables" list and press "Edit"
8.  Click "New" and add the following to the new line that appears:
      %JAVA_HOME%\bin
9.  Press "Ok"
10. Click on the "New" button under "System Variables"
5.  Add the following (the quotes (") are important!!):
      Variable name: PATH_TO_FX
      Variable value: "C:\Program Files\Java\javafx-sdk-12.0.1\lib" (or where javafx folder is installed on your computer)
6.  Click "Ok"
7.  Restart the computer so the new Environment Variables become active


Guide for Mac OSX
1.  open terminal
2.  run command = cd ~/
3.  run command = nano .bash_profile
4.  add following lines at the end of the document and change directory of last one to the location you unzipped javafx:
	  export JAVA_HOME=$(/usr/libexec/java_home)
	  export PATH=$PATH:$JAVAHOME/bin
	  export PATH_TO_FX= location/of/javafx-sdk-12.0.1/lib
5. save and exit with "ctrl + o" and "ctrl + x"
6. source ~/.bash_profile

Now your enviromental variables should be set up for running the GUI

The ofmcGUI.jar file is not runnable so it has to be launched with the run.bat file or a command in terminal.

To run the GUI on windows you use the batfile run.bat

A script has not been made yet to run the GUI for Mac and therefore it needs to be ran from the terminal:
java -jar --module-path $PATH_TO_FX --add-modules=javafx.controls,javafx.fxml,javafx.graphics --add-exports javafx.graphics/com.sun.javafx.geom=ALL-UNNAMED --add-exports javafx.graphics/com.sun.javafx.scene.text=ALL-UNNAMED --add-exports javafx.graphics/com.sun.javafx.text=ALL-UNNAMED --add-opens javafx.graphics/javafx.scene=ALL-UNNAMED --add-opens javafx.graphics/javafx.scene.text=ALL-UNNAMED --add-opens javafx.graphics/com.sun.javafx.text=ALL-UNNAMED OFMCGUI.jar



Please make sure that ofmc.exe is located in the same folder as the ofmcGUI.jar file.
Important : it should be named "ofmc.exe"



If you find any errors or simply have ideas for improvements we kindly ask you to send
us an e-mail to:

s165544@student.dtu.dk
or
s144113@student.dtu.dk


