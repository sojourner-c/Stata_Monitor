# Stata Monitor
Run .do file in batch mode and receive email stating if .do failed.

# Installation and Use Instructions

## A. Downloading Python

1. Download Python from the Python [website](https://www.python.org/downloads/) and download the most recent version.
2. Run the .exe that downloads to your machine
     * In the "Install Python" screen if you would like to accept the default install simply click "Install NOW".
     * If you do not want to accept default install (for example if you don't have write access to the C drive) click "Customize installation".
     * In the "Advanced Options" screen under "Customize install location" enter the location you prefer to install python followed by the default name of the python folder.
     * Finally click "Install".

## B. Cloning the Stata Monitor Repository

1. Create a folder in a desired directory to store the monitor.
2. Download the package by clicking *Download Zip* on the right hand side of the screen on the [Stata Monitor github page](https://github.com/sojourner-c/Stata_Monitor). 
3. Move the .zip file to the desired directory and unzip the file. Alternatively, with [Git](https://github.com/) installed, cd into the desired directory and run:
`git clone https://github.com/sojourner-c/Stata_Monitor.git`.

## C. Install Python Dependencies

1. Open a command prompt.
2. Type `pip install pypiwin32` and hit enter.

# Using Stata Monitor

1. Open a command prompt.
2. cd to base level of the Stata Monitor.
3. Type `python` and hit enter.
4. Type `from lib import stata_monitor` and hit enter.
5. Create a python variable with the full path and file name of the .do file you wish to run. For example, a .do file named "test.do" the directory "C:\stata\do" type `file = r"C:\stata\do\test.do"` and hit enter.
6. Type `stata_monitor.stata_monitor(file)` and hit enter. Replace file with whatever you named your python variable or with a raw string off the full path and file name.


# Testing Python Updates
Changes to the Python scripts or Modules can be tested by running the unittests located in the "tests" folder.

1. Open a command prompt.
2. cd to base level of the Stata Monitor.
3. Enter `python -m unittest discover -s tests` and hit enter.
4. If necessary edit the changes made until the tests run without failures.
