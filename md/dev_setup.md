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
Installation guides for the plugins are on their respective pages:

* [Language Support for Java(TM) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)
* [Debugger for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
* [Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)

**You must restart VSCode after installing and configuring the extensions.**

In order, these plugins add the following functionality:
* The ability to **build** programs using the JDK
* The ability to **run** built Java programs
* **Intelligent autocomplete** when writing Java

#### Configuring Language Support for Java
You may have to configure the Language Support extension to use your installed JDK.  
To do this, in VSCode:
* Go to `File > Preferences > Settings`
* In the search bar on the settings page, search for **"java.home"**
* Click `Edit in settings.json`
* Paste the path/location of your java installation inbetween the quotation marks for `java.home`, and save. The entry should look like the below, substituting for your JDK install location:
```
"java.home": "/Library/Java/JavaVirtualMachines/AdoptOpenJDK-<version>.jdk"
```

## Download the Course Code
We will use VSCode to download the code for the project.

Under the hood this is using a tool called **git** - which developers use to control changes to the code.

To download the source code:
* Go to `View > SCM` or press `Ctrl+Shift+G`
* Click "Clone Repository"
* In the Repository URL box, paste `https://github.com/Ben-Woolley/java-for-beginners.git`
* Select where you want to download the code to, e.g. a new folder `projects` in my Documents.

To open the code in VSCode go to `File > Open Folder`, select the folder `java-for-beginners` and click OK.

## Verify your Installation
To confirm you can run Java programs, open `Main.java` by clicking on it in the explorer window. Click the `run` button below line 4 in the file.

If the program runs (i.e. a box opens that says `Congratulations, you can build and run Java files!`) then you are ready to go.