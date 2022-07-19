### Python installation:

* Download exe file from [the official website](https://www.python.org/downloads/) 
* Check the installed path:  
  * Type `start %appdata%` in cmd 
  * From the popped up folder `..\AppData\Roaming` navigate to `..\AppData\Local` folder
  * Locate python in the folder
    * On Windows 10, default directory for Python 3.x is `Local\Programs\Python`

### PATH setup to enable `pip` in the command line

* Check if a path is already set up:  
  * In CMD prompt type: `echo %PATH%` 
* Find path of pip: 
  * In CMD prompt type: `start %appdata%` to trigger pop up 
  * From the popped up folder `..\AppData\Roaming` navigate to `..\AppData\Local` folder 
  * Locate pip in the folder 
    * On Windows 10, default directory for pip is `Local\Programs\Python\Python3x\Scripts` 
  * Copy the directory path from the address bar 
* Set up the environment (either works) 
  * From Command Line 
    * Type `setx PATH "%PATH%;COPY YOUR PATH HERE"`
  * From Control Panel 
    * From the start icon, navigate to Control Panel > System and Security > System. 
    * Go to Advanced System Setting on the sidebar 
    * Go to Environmental Variables 
    * Click on Path and then Edit 
    * Add a new path by clicking on New and paste the path 
    * Click OK three times to preserve the change 
* Check the set up 
  * Close the cmd prompt and open a new one 
  * In the new cmd prompt type `echo %PATH%` to check if the path is shown 

### Geopandas installation 

* `pip install wheel` :  a package used to configure wheel files which are used to install geopandas dependencies 
* In one folder, download the following geopandas dependencies from the [Unofficial Windows Binaries for Python Extension Packages](http://pythonic.zoomquiet.top/data/20101216091618/index.html) website based on your Python installation: 
  * GDAL 
  * Fiona 
  * Pyproj 
  * Rtree 

    _Example_: for Python 3.x installed, download: 
    * GDAL-version-cp3x-cp3xm-win-amd64.whl 
    * Fiona-version-cp3x-cp3xm-win-amd64.whl 
    * pyproj-version-cp3x-cp3xm-win-amd64.whl 
    * Rtree-version-cp3x-cp3xm-win-amd64.whl 

* In cmd prompt navigate to the folder where the dependencies are downloaded 
  * Open a cmd prompt 
  * Type `cd YOUR FOLDER PATH` 
* Install dependencies in the following order: 
  * `pip install .\GDAL-version-cp3x-cp3xm-win-amd64.whl` 
  * `pip install .\Fiona-version-cp3x-cp3xm-win-amd64.whl` 
  * `pip install .\pyproj-version-cp3x-cp3xm-win-amd64.whl` 
  * `pip install .\Rtree-version-cp3x-cp3xm-win-amd64.whl` 
* If no error, proceed to install geopandas by typing `pip install geopandas` in the cmd line

#### Referenced links: 
+ https://stackoverflow.com/questions/56958421/pip-install-geopandas-on-windows  
+ https://towardsdatascience.com/geopandas-installation-the-easy-way-for-windows-31a666b3610f
+ https://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command  
