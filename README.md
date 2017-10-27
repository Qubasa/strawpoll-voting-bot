# Description
A voting bot written in python 3.x for strawpoll.de. It uses a proxy list to vote multiple times in a survey.
It works on Mac, Windows and Linux.

### Features
- Easy to use command line driven program
- 270 proxies are given from the get-go. More can be easily added
- The program saves already used proxies in an xml file to enhance the voting speed dramatically

# Usage
```
Usage: Main.py [options]

Options:
  -h, --help            show this help message and exit
  -v VOTES, --votes=VOTES
                        number of votes to give
  -s SURVEY, --survey=SURVEY
                        id of the survey
  -t TARGET, --target=TARGET
                        checkbox to vote for
  -f, --flush           Deletes skipping proxy list
```

### Example
```
python Main.py -v 10 -s abbcw17 -t check3537987
```

# How to install it ?
Download the zip or clone it with git then install the required library with:
```
pip install requests
```

## What is pip? I don't understand!
If you don't understand how to install a library also called a "module" in Python please go checkout YT: 
[How to download and install Python Packages and Modules with Pip](https://www.youtube.com/watch?v=jnpC_Ib_lbc)

# How to add proxies to the list
Download [Libre Office](https://www.libreoffice.org/) open up the LibreOffice writer.
Paste on each new line the proxy IP and a port divided by a colon.
Example:
```
149.56.160.23:80
193.108.38.23:80
94.56.130.89:3128
```
Save the file as an .xml file and replace the https-proxy-list.xml file in the project directory.

# How do I get the survey id and the target ?
The survey id is always in the url pointing to your survey for example: https://strawpoll.de/abbcw17 then abbcw17 would be the id.
To find the target you have to right click the checkbox you want to vote for, then go to inspect element and search for a
value with 'check' at the beginning like check3537987. This is the checkbox id.
