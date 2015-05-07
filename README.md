# SecureCRT_Python_Scripts
This script was created to automate the collection of PRE, POST, and subsequent differential data during network changes.  The script, as the name implies, is called by the SecureCRT application and is written, in this iteration, specifically to the SecureCRT API.  The current version of SecureCRT, v7.3.3 (x64 build 779) is compatible with Python v2.6.  The script contains options to execute in PRE/POST mode, as well as Single/Multiple device mode.  Each decision point is conveyed via a pop-up selection box, to maximize ease of use. 

Using the Script:
- Place the script in a/the directory which will be the repository of the output data collected, as the output files generated are created in the root directory which the script resides in.  In keeping with the spirit/purpose of this script, create a specific local directory for a given change and locate the script therein.  
- The script calls 2 different flat files during operation:
-   1.)  A device list - List all the devices involved in the change; one per line, with no white space at the top, or trailing
-       a.) Required when running script in 'Multiple Device' mode.
-       b.) *This iteration assumes use on the HPNA platform (v9.2.2 tested); a successful SSH connection (via SecureCRT) is required prior to executing the script.
-   2.)  A command list - List all the 'show' commands required, in the exact CLI syntax; one per line.
-   For each device listed, the command list is executed in a top-down, line-by-line fashion.
- As the command list is completed for each device on the device list, a file containing the command outputs is generated, with a filename in the following format: PRE/POST_TEST_devicename.txt
- If script is executed in with the 'POST' option, a dialogue box to perform a differential function will pop-up after the last POST test file is generated.  If the function is performed, files will be created with the following filename format: 'DIFF_devicename.txt'.


**A road-map is underway for increased functionality and application/platform flexibility.  Be sure to check back periodically for updates. 
***Feature requests, as well as functionality feedback is welcomed!

**** Although the code has been tested, the code is delivered as is, with no guarantees.****
