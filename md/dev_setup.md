# Development Setup Guide
This guide will set up your development environment, ready for writing code for the rest of the course.  
We will download/install:
* The Java JDK
* An IDE - Visual Studio Code (or VSCode)
* The Java 101 code

## Install a Java JDK
We're going to use AdoptOpenJDK, an open-source distribution of Java.

**You can download the installer from [here](https://adoptopenjdk.net/archive.html?variant=openjdk14&jvmVariant=hotspot).**  
The link points to Java 14, but feel free to use a more recent version.

AdoptOpenJDK installer guide: https://adoptopenjdk.net/installation.html  

## Windows
1. Download the latest **JDK** **Installer** for **Windows x64**. The downloaded file should be a **.msi** file.
2. Follow the official installation guide found [here](https://adoptopenjdk.net/installation.html?variant=openjdk14&jvmVariant=hotspot#windows-msi) **with these modifications at step 3:**
   * Allow the installer to update JAVA_HOME
   
Your JDK installation will be at `C:\Program Files\AdoptOpenJDK\<here>\`.

## Mac
1. Download the latest **JDK** **Installer** for **MaxOS x64**. The downloaded file should be a **.pkg** file.
2. Follow the official installation guide found [here](https://adoptopenjdk.net/installation.html?variant=openjdk14&jvmVariant=hotspot#macos-pkg)

Your JDK installation will be at `/Library/Java/JavaVirtualMachines/AdoptOpenJDK-<version>.<jdk|jre>/`

## Install VSCode
To effectively write Java programs, most developers use an IDE (Integrated Development Environment).

Our IDE of choice for this course is Visual Studio Code - a lightweight editor that can be greatly extended with plugins.

**Download and install VSCode from https://code.visualstudio.com**

### Required Extensions
VSCode is not natively a Java IDE, so we need to install some extensions to make writing, building, and running Java code simple.  
You can install the plugins by following the links and clicking the Install button. Or you can search by their names in the Extensions ![Extensions icon](/images/setup/extensions_icon.png) sidebar.

* [Language Support for Java(TM) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)
* [Debugger for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
* [Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)

**You must restart VSCode after installing and configuring the extensions.**

In order, these plugins add the following functionality:
* The ability to **build** programs using the JDK
* The ability to **run** built Java programs
* **Intelligent autocomplete** when writing Java

#### (Optional) Configuring Language Support for Java
**If the Java extension reports an error** you may have to configure the Language Support extension to use your installed JDK.  
To do this, in VSCode:
* Go to `File > Preferences > Settings`
* In the search bar on the settings page, search for **"java.home"**, then click `Edit in settings.json`
![Java home option](/images/setup/java_home_set.png)
* Paste the path/location of your java installation inbetween the quotation marks for `java.home`, and save. The entry should look like the below, substituting for your JDK install location:  
![Java home json](/images/setup/java_home_json.png)

## Download the Course Code
To download the source code:
* Download the course code zip file from [here](https://github.com/Ben-Woolley/java-for-beginners/archive/master.zip)
* Select where you want to keep your code to, e.g. a new folder `projects` in my Documents.
* Unpack the zip file to your projects folder

To open the code in VSCode go to `File > Open Folder`, select the folder `java-for-beginners-master` and click OK.

## Verify your Installation
To confirm you can run Java programs:
* Go to the Explorer menu by clicking the Explorer icon ![Explorer icon](/images/setup/explorer_icon.png)
* Navigate to `Main.java` by clicking on it in the explorer window.  
![Explorer window with Main.java open](/images/setup/explorer_main.png)
* Run `Main.java` by either:
   * Clicking on the Run icon ![Run icon](/images/setup/run_icon.png), and clicking the `Run and debug` button.
   * Clicking the `run` button above line five in `Main.java`

![Explorer window with run buttons highlighted](/images/setup/run_java.png)

If the program runs (i.e. a box opens that says `Congratulations, you can build and run Java files!`) then you are ready to go.