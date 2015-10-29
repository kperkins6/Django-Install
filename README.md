# Django-Install 

##Before We Begin
  * We will be covering the installation of the following:
    - Python
    - Setuptools 
    - PIP
    - Django
  * The following will cover an Installation for OS X and Windows.  Linux to come soon.  

####Please Select Your Operating system below:
  * [Mac OS X](#macInstall)  
  * [Linux](#linuxInstall)  
  * [Windows](#windowsInstall)  


<a name="macInstall"></a>
##Mac OS X Installation
####Installing Python
1. Make sure **Xcode Command Line Tools** are installed  
  **Option 1** (takes up less space)  
    * Open a terminal window  
    * Retrieve the most recent Xcode tools by typing the following command:  
      <pre>xcode-select –install</pre>
    (note: if you receive an error saying already installed, just keep moving)

  **Option 2** (takes up more space)  
    * Download the full Xcode files from Apple: [Xcode](https://developer.apple.com/xcode/download/)
    * Once fully downloaded, install and proceed
    
2. Make sure **Homebrew** is installed.  
  * We need **brew** in order to download pyton and several other important essentials for this project. We are able to use the following script to install brew and learn what it's adding:
    <pre>ruby -e “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”</pre>
  * Press ENTER and enter your password to allow the install
  * To ensure everything worked, type the following:
    <pre>brew doctor</pre>
  * Once you’ve installed Homebrew, insert the Homebrew directory at the top of your PATH environment variable. You can do this by adding the following line at the bottom of your *~/.profile* file[2]
    <pre>export PATH=/usr/local/bin:/usr/local/sbin:$PATH</pre>
  * You may also install **Homebrew Cask**[4], which allows for downloading larger OS X applications and binaries, but we won't need it for this project. You can install via the command line with this command:
    <pre>brew install caskroom/cask/brew-cask</pre>

3. Let's Get Python!
  * We can start by simply typing the following into a terminal:
    <pre>brew install python</pre>
  * "Homebrew installs Setuptools and pip for you. Setuptools enables you to download and install any compliant Python software over a network with a single command (easy_install). It also enables you to add this network installation capability to your own Python software with very little work. pip is a tool for easily installing and managing Python packages, that is recommended over easy_install. It is superior to easy_install in several ways, and is actively maintained."[2]
  * *If you want* to ensure you have pip and python, fully quit out of the terminal application.  Open up a new terminal and type:
   <pre>which python</pre> 
   and
   <pre>which pip</pre>
  * Congratulations, you now have Python!  
  * Note: You can check the version of python by typing the following into your terminal window
  <pre> python --version </pre>

####Installing Django
#####Before We Begin
  * Make sure you have Python, Setuptools, and PIP.
  * If you do not, install them now.  You can follow the guide above.  

1. Using PIP, we will install Django
  * To Install Django, all we need to do is open a command prompt and type:
    <pre>pip install django</pre>
  * When finished, you can type:
    <pre>django-admin --version</pre>

##Starting up Django
####Before We Begin
  * Coming Soon
  

######End of Mac Installation


<a name="windowsInstall"></a>
##Windows Installation 
####Installing Python
1. Downloading Python from the source
  * The first place we can go is Python's website.  Head to this link to grab the Windows MSI Installer:
    <pre>https://www.python.org/downloads/</pre>
  * Follow the installer's instructions on-screen
  * After installation, open the command prompt and check the installed version using the following command: 
   <pre>python --version</pre>
    "If you encounter a problem, make sure you have set the **PATH** variable correctly. You might need to adjust your **PATH** environment variable to include paths to the Python executable and additional scripts. For example, if your Python is installed in **C:\Python34\**, the following paths need to be added to **PATH**" [4]:
<pre>C:\Python34\;C:\Python34\Scripts;</pre>
2. Download Setuptools
  * Setuptools is necessary for downloading Python Packages
  * You can directly download the file [ez_setup.py](https://bootstrap.pypa.io/ez_setup.py) by right clicking, save link as.  
  * Once downloaded, it is as simple as right clicking and running the program
  * You can go to [Python's Setuptools page](https://pypi.python.org/pypi/setuptools) for more details.
3. Install PIP
  * PIP is a Python Package Manager using the Python Package Index.  Thankfully, it's pretty straight forward to install.
  * Open up a command prompt and type:
    <pre>easy_install pip</pre>
  * If these steps do not work, try restarting command prompt or your computer to make sure setuptools had a chance to start.
  * If that didn't help, head to [this install guide](https://pip.pypa.io/en/latest/installing/) for pip
4. You now have all the Python tools you need to get started!

####Installing Django
#####Before We Begin
  * Make sure you have Python, Setuptools, and PIP.
  * If you do not, install them now.  You can follow the guide above.  

1. Using PIP, we will install Django
  * Thankfully, all of the previous steps had the hard work.
  * To Install Django, all we need to do is open a command prompt and type:
    <pre>pip install django</pre>
  * When finished, you can type:
    <pre>django-admin --version</pre>
  * Once you get Django up and running, if the help text is displayed endlessly, you can try this solution:
    > If django-admin only displays the help text no matter what arguments
    > it is given, there is probably a problem with the file association in
    > Windows. Check if there is more than one environment variable set for 
    > running Python scripts in **PATH**. This usually occurs when there is more
    > than one Python version installed.
    
  * If using a proxy and hitting issues, here is a fix direct from Django's Guide:  
    > If you are connecting to the internet behind a proxy, there might be problem in
    > running the commands **easy_install pip** and **pip install django**. Set the environment 
    > variables for proxy configuration in the command prompt as follows:
    > <pre>set http_proxy=http://username:password@proxyserver:proxyport
    set https_proxy=https://username:password@proxyserver:proxyport</pre>

2. You're finished!

##Starting up Django
####Before We Begin
  * Coming Soon

######End of Windows Installation


<a name="linuxInstall"></a>
##Linux Installation 

####Installing Python
1.The first step is to install python. Generally most Linux Operating Systems have Python 2.7 installed by default.  
  * To check if it is already installed, use the following command:
    <pre>python --version</pre>
  * You should get an output similar to:
    <pre>Python 2.7.6</pre>
  * If not, then python can be downloaded from [Python's Website](https://www.python.org/)

####Installing a Database system(SQLite)
1. Since most of the web applications need a database and querying has to be done upon it, it's better to have a database setup on your system.  
  * SQLite is a database we can use, it is a light weight database and its good enough to begin with. For any simple web applications that you develop, you can use SQLite itself and later upgrade it to suit your needs. 
  * Some linux systems have SQLite preinstalled along with python. If you already have it, the command below can be ignored.
  * To install SQLite, use the following command:
  <pre>sudo apt-get install sqlite</pre>  

####Installing pip and easy_install
1. Any previous versions of Django if existing has to be removed. But if you have (pip) and (easy_install) for installation then you do not have to worry about removing the previous versions because this will be handled already.
  * Install both of them by using the following command:
    <pre>sudo apt-get install python-setuptools</pre>
  * The above command installs the required python setup tools along with easy_install. In most cases, "pip" is preinstalled. If it isn't, install pip as given in the official documentation on [pip's website](https://pip.pypa.io/en/latest/installing/)

2. Before proceeding, confirm that python, SQLite, pip and easy_install has been installed. To do so, use the commands one after another:
  * Command:
    <pre>python --version</pre>
  * Output should be something similar to: 
    <pre>Python 2.7.6</pre>
  * Command:
    <pre>sqlite -version</pre>
  * Output should be something similar to:
    <pre>2.8.27</pre>
  * Command:
    <pre>pip --version</pre>
  * Output should be something similar to: 
    <pre>pip 7.1.2 from /usr/local/lib/python2.7/dist-packages (python 2.7)</pre>
  * Command:
    <pre>easy_install --version</pre>
  * Output should be something similar to: 
    <pre>setuptools 18.3.2 from usr/local/lib/python2.7/dist-packages/setuptools-18.3.2-py2.7.egg (Python 2.7)</pre>
  * If there are any issues, please go back a few steps and attempt to re-install.

#### Installing a virtual enviornment
1. In this step, we install a "Virtual Environment." After a lot of searching and testing, I found that Django can be run very easily on a virtual environment. A virtual environment is created to encapsulate all the data and resources required to run Django at one place so that all the changes made remain in that environment itself. Another important benefit of the virtual environment is that it supports the light weight web server provided by Django by default. This allows the installation and integration of apache server to be avoided.
  * The easiest way to install a virtual environment on linux is by using the "easy_install" command. This script comes with a package called python-setuptools which we have installed in a previous step. 
  * We can install the environment using the following command:
    <pre>sudo easy_install virtualenv</pre>
  * Be patient, as it may take some time depending on the network

#### Creating and setting up the virtual environment
1. Now we create a folder using virtualenv so that the folder can act as the virtual environment to contain Django. 
  * Type the following command in the terminal:
    <pre>virtualenv --no-site-packages django-user</pre>

2. Here django-user is the folder that will be created and used as the environment. It will be created under the directory you are currently in. 
  * To start the environment use the command:
    <pre>source django-user/bin/activate</pre>

3. Now if you see your folder name at the beginning of the prompt, it means that the environment is started.
  * You should be able to see:
    <pre>(django-user)</pre>

4. Navigate to the folder django-user
  * Use the following command:
    <pre>cd django-user</pre>
  * Then list the items in the folder using this command:
    <pre>ls</pre>
  * You should be able to see directories like bin, lib, include, local. 

5. What does this environment do?
  * Any command or operation performed in the environment will not affect anything outside the environment. The changes are isolated and this allows us to easily create as many environments as we want and test many things very easily without causing problems for other projects.

####Installing Django
1. The final step is installing Django within this environment that we have created in the previous step. Remember that you still have to be in the virtual environment in the django-user folder else django will be installed outside the environmant and cannot be used. To install Django use the command:
  <pre>easy_install django</pre>
2. Thats it! Django is installed on your system with all required functionality for beginners to develop and learn the framework.  
3. Now you can go ahead and try out the DJANGO tutorial to learn the different functionalities and run your first web app. You can find the tutorial in the official [Django documentation](https://docs.djangoproject.com/en/1.7/intro/tutorial01/#creating-a-project)

####Starting up Django

#####Before We Begin
  * Coming Soon

######End of Linux Installation


##References
1. Homebrew for OS X install: http://www.howtogeek.com/211541/homebrew-for-os-x-easily-installs-desktop-apps-and-terminal-utilities/
2. Python Install : http://docs.python-guide.org/en/latest/starting/install/osx/
3. Django Install Windows: https://docs.djangoproject.com/en/1.8/howto/windows/
4. Cask by Homebrew : http://caskroom.io/
5. Linux Django Install : https://www.howtoforge.com/tutorial/django-install-ubuntu-14.04/
