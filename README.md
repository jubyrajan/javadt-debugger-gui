# javadt-debugger-gui
Steps to build GUI for javadt debugger. This is the experimental javadt debug UI provided with JDK samples.

Create two local folders **src** and **bin**. Copy source code from the **jpda** folder in http://download.oracle.com/otn-pub/java/jdk/8u152-b16-demos/aa0333dd3019491ca4f6ddbe78cdb6d0/jdk-8u152-windows-x64-demos.zip into **src** folder.

**Screenshot:**

![Debug Window](https://raw.githubusercontent.com/jubyrajan/javadt-debugger-gui/master/screenshot.png)

**USAGE:**

    java -cp .;%JAVA_HOME%\lib\tools.jar;javadt.jar com.sun.tools.example.debug.gui.GUI -sourcepath path_to_source_folder

The -sourcepath path_to_source_folder is optional, and can be ignored if not needed.
    
**Compiling:**
Go to src folder and run the following command:

    javac -d ../bin com\sun\tools\example\debug\bdi\*.java com\sun\tools\example\debug\event\*.java com\sun\tools\example\debug\expr\*.java com\sun\tools\example\debug\gui\*.java com\sun\tools\example\debug\tty\*.java

**Creating a jar from the compiled classes:**
Go to bin folder after compiling the sources and run the following command:

    jar cvfe javadt.jar com.sun.tools.example.debug.gui.GUI *.class

**Execute from src folder:**

    java -cp .;%JAVA_HOME%\tools.jar com.sun.tools.example.debug.gui.GUI -sourcepath path_to_source_folder

