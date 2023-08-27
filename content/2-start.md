---
title: Install and Run Refine
nav: Start
---

To use Refine you will need a web browser (Chrome or Firefox) and an [OpenRefine kit](https://openrefine.org/download.html). 

Check the [official installation documentation](https://openrefine.org/docs/manual/installing) or follow the quick instructions for your system below:

{% capture windows %}
- **Download:** visit the [Refine download page](https://openrefine.org/download.html) and choose the latest version for Windows "with embedded Java". This is a self contained zip package that includes everything needed to run Refine on your system.
- **Extract:** the package you downloaded will be a zip file that needs to be extracted (e.g. "openrefine-win-with-java-3.7.4.zip"). Unzip the package by right clicking and selecting Extract All. Move the resulting folder to a sensible permanent location on your computer, e.g. "C:\openrefine\" or Documents.
- **Run:** inside the folder you extracted, double click "openrefine.exe" to start Refine. The first time you may get a warning that the publisher could not be verified, dismiss the warning and click *Run*. Once open, pin the Refine icon to your taskbar for easy access in the future! 

*Note:* if you would like to use the traditional Refine kit, check [notes on installing Java on Windows]({{ '/content/win-java.html' | relative_url }}).
{% endcapture %}
{% capture mac %}
- **Download:** visit the [Refine download page](https://openrefine.org/download.html) and choose the latest version for Mac OS. This is a self contained package that includes everything needed to run Refine on your system (e.g. "openrefine-mac-3.7.4.dmg").
- **Install:** drag the Refine icon from your downloads to the Applications folder.
- **Run:** click the Refine icon in your Applications folder. Usually the first time running the program you will get a security warning--you will need to right-click/two finger click and select "Open" from the context menu, then click "Open" on the security warning.
{% endcapture %}
{% capture linux %}
To install the most recent version of Refine, it is best to install Java, then download the current version of Refine.

- **Java:** if you do not have Java JRE/JDK, install latest Java from your distro's repositories. For example, on Ubuntu/Debian: `sudo apt install default-jre`
- **Download:** visit the [Refine download page](https://openrefine.org/download.html) and choose the latest version for Linux.
- **Extract:** the package you downloaded will be a compressed archive (e.g. "openrefine-linux-3.7.4.tar.gz"). Unpack the file using your Archive manager or Tar (e.g. `tar xzf openrefine-linux-3.7.4.tar.gz`) to a sensible permanent location (e.g. in your Home directory).
- **Run:** open a terminal in your OpenRefine directory and type `./refine`.

Alternatively, it is possible to install from some distribution repositories, e.g. `sudo apt install openrefine`.
{% endcapture %}
{% include accordion.html title1="Windows" text1=windows title2="Mac" text2=mac title3="Linux" text3=linux %}

If you plan on working with large data files over one million cells or 50 MB, check out [Increasing memory allocation](https://openrefine.org/docs/manual/installing#increasing-memory-allocation).

*Note:* In the past, installing Java was required so you may see this mentioned in tutorials--however, this is *no longer necessary* on Windows and Mac!

## Use Refine

There are two parts to Refine: 

- <span class="term">Terminal Window:</span> Starting Refine differs depending on your OS (see above), but in all cases the app will start running in a terminal window. This is the Refine application running in Java. You can ignore and minimize the terminal window (but do not close!). If something isn't working, you can check here for error messages.
- <span class="term">GUI Interface:</span> Once Refine is running in a terminal, your default web browser should automatically open with the interface--which is a "web page" in your browser. If it does not open automatically, you close the browser tab, or you want to use a different browser, you can find the GUI by typing <http://127.0.0.1:3333> or `localhost:3333` in your address bar. 

{% include figure.html img="openrefine.png" alt="OpenRefine terminal and GUI" %}

To <span class="term">shut down</span> close any Refine tabs you have open in your browser, then stop the host terminal window with `Ctrl+C` (or `Command-Q` on Mac). 
This will ensure any open projects are safely saved.

{% include alert.html text="The user interface is rendered by your web browser, but Refine is not a web application. 
Although it uses the term *upload* and *download*, **no information is sent online and no internet connection is necessary**.
For best results, use Chrome, Chromium, or Firefox browser." color="success" %}

## Update Your Version of OpenRefine

OpenRefine gets [regular updates](https://openrefine.org/whats_new) which fix bugs, improve features, and ensure security.
A banner notice will appear at the top of the home screen when starting Refine if an update is available.

In general, your old version will keep working just fine--but *unless you are using extensions that may not be compatible with new versions*, you will probably want to upgrade to get the latest fixes!

There is no automatic updater, so upgrading is a manual process identical to your first installation. 
Visit the [Refine download page](https://openrefine.org/download), get the appropriate package, and extract to a sensible location. 
On Windows and Linux, you can leave your existing version in its current location until you test the new one.
Once you are sure everything is working, delete the entire folder containing the old version. 

Note that your project data is stored in a separate "workspace" directory, so your past projects will still be available after updating.
If your "workspace" contains critical data, it is a good practice to backup the folder before upgrading *or* ensure you have exported copies of the projects.
To find your "workspace", click the "Open project" tab on the Refine start page side bar, then look at the bottom of the screen and click on "Browse workspace directory". 
This should open a file explorer window on your system in the "workspace" folder (see [where data is stored](https://openrefine.org/docs/manual/installing#set-where-data-is-stored){:target='_blank' rel='noopener'}).

You can find details about different Refine versions on the [Release notes](https://openrefine.org/whats_new) or the [GitHub Releases](https://github.com/OpenRefine/OpenRefine/releases).
