---
title: Install and Run Refine
nav: Start
---

To use Refine you will need a web browser (Firefox or Chrome) and an [OpenRefine kit](https://openrefine.org/download.html). 

In the past, [installing Java]({{ '/content/win-java.html' | relative_url }}) was required--however, this is *no longer necessary* on Windows and Mac!
Check the [official installation documentation](https://docs.openrefine.org/manual/installing) or follow the instructions for your system below:

{% capture windows %}
- **Download:** visit the [Refine download page](https://openrefine.org/download.html) and choose the latest "Windows kit with embedded Java" package. This is a self contained package that includes everything needed to run Refine on your system.
- **Extract:** the package you downloaded will be a zip file that needs to be extracted (e.g. "openrefine-win-with-java-3.4.1.zip"). Unzip the package by right clicking and selecting Extract All. Move the resulting folder to a sensible permanent location on your computer, e.g. "C:\openrefine\" or Documents.
- **Run:** inside the folder you extracted, double click "openrefine.exe" to start Refine. The first time you may get a warning that the publisher could not be verified, dismiss the warning and click *Run*. Once open, pin the Refine icon to your taskbar for easy access in the future! 

*Note:* if you would like to use the traditional Refine kit, check [notes on installing Java on Windows]({{ '/content/win-java.html' | relative_url }}).
{% endcapture %}
{% capture mac %}
- **Download:** visit the [Refine download page](https://openrefine.org/download.html) and choose the latest "Mac kit". This is a self contained package that includes everything needed to run Refine on your system (e.g. "openrefine-mac-3.4.1.dmg").
- **Install:** drag the Refine kit from your downloads to the Applications folder.
- **Run:** click the Refine icon in your Applications folder. 
{% endcapture %}
{% capture linux %}
- **Java:** if you do not have Java JRE/JDK, install latest Java from your distro's repositories. For example, on Ubuntu/Debian: `sudo apt install default-jre`
- **Download:** visit the [Refine download page](https://openrefine.org/download.html) and choose the latest "Linux kit".
- **Extract:** the package you downloaded will be a compressed archive (e.g. "openrefine-linux-3.4.1.tar.gz"). Unpack the file using your Archive manager or Tar (e.g. `tar xzf openrefine-linux-3.4.1.tar.gz`) to a sensible permanent location (e.g. in your Home directory).
- **Run:** open a terminal in your OpenRefine directory and type `./refine`.
{% endcapture %}
{% include accordion.html title1="Windows" text1=windows title2="Mac" text2=mac title3="Linux" text3=linux %}

## Use Refine

There are two parts to Refine: 

- <span class="term">Terminal Window:</span> Starting Refine differs depending on your OS (see above), but in all cases the app will start running in a terminal window. This is the Refine application running in Java. You can ignore and minimize the terminal window (but do not close!). If something isn't working, you can check here for error messages.
- <span class="term">GUI Interface:</span> Once Refine is running in a terminal, your default web browser should automatically open with the interface--which is a "web page" in your browser. If it does not open automatically or you close the browser tab, find the GUI by typing <http://127.0.0.1:3333> or `localhost:3333` in your address bar. 

{% include figure.html img="openrefine.png" alt="OpenRefine terminal and GUI" %}

To <span class="term">shut down</span> close any Refine tabs you have open in your browser, then stop the host terminal window with `Ctrl+C` (or `Command-Q` on Mac). 
This will ensure any open projects are safely saved.

{% include alert.html text="The user interface is rendered by your web browser, but Refine is not a web application. 
Although it uses the term *upload* and *download*, **no information is sent online and no internet connection is necessary**.
For best results, use Firefox, Chrome, or Chromium browser." color="success" %}
