# Bget
Table of Contents
1. 	Introduction
2.	Features
3.	Running Bget
4.	Switches
	a.	GET
	b.	PASTEBIN
	c.	REMOVE
	d.	Update
	e.	INFO
	f.	LIST
	g.	UPGRADE
	h.	HELP
5.	Methods
	a.	Jscript -JS
	b.	Visual Basic Script -VBS
	c.	Powershell -PS
	d.	BITSAdmin -BITS
	e.	CURL

## INTRODUCTION
Bget is a batch-file command-line tool for handling Windows scripts. It is built to be a companion to those who write, use and maintain Windows scripts. It helps those who use scripts easily download, update and remove scripts. It’s built for scripters, by scripters.

## Features
1.	Download scripts from the Bget server: These scripts are vetted and sorted by us. We’ve gone about curating some of the most interesting scripts we could find that we think would be interesting and useful to you as well.
2.	Download scripts from Pastebin: Pastebin has long been the coder’s friend, and so we added the ability to fetch scripts from Pastebin. These scripts are not pre-vetted however, but they offer the ability for fast code downloading without waiting for us to vet them.
3.	Update scripts: Rather than manually re-download the latest version of every script, Bget handles that for you, getting the latest version of any script you’ve downloaded.
4.	Easily remove scripts: Don’t like a script you downloaded? Easily remove it with Bget. One command and it’s buh-bye script.
5.	View script info: This allows you to see basic information about a script such as its name, author and description, allowing you to make an informed decision before downloading.
6.	Bget also allows you to list all scripts on the server and list downloaded scripts on the local computer.
7.	Upgrade feature: Bget also updates itself so you always stay up-to-date.
8.	Multiple download methods: Bget has many ways to get a script. These are: Jscript, VBScript, Powershell, BITSAdmin and CURL.
Running Bget
Captain Obvious: Bget is a command-line tool, so it needs to be run from the command line. A typical Bget command looks like this:
Bget [-switch] [-method] SCRIPT
Here’s an example:
Scenario: You want to fetch a script from the server called “test”.  The easiest way to do this would be:
BGET -get -usecurl test

## Switches

### -Get: This is the script fetching function.
Usage:
BGET -get -usemethod script
Supported methods: JS, VBS, PS, CURL, BITS
Example: BGET -get -usevbs test
The above will download the script named “test” from the Bget server using the VBS download function.

### -Pastebin: This fetches a pastebin raw and saves it as a .bat script.
Usage:
BGET -pastebin -usemethod PASTECODE
Supported methods: JS, VBS, PS, CURL.
BITSADMIN (BITS method) is not compatible with the -pastebin switch.
Example:
BGET -pastebin -usecurl 1wsBxRs4
The paste code is the unique element of a Pastebin URL.
i.e., A Pastebin script located at https://pastebin.com/YkEtQYFR would have YkEtQYFR as its paste code. If you get the paste code wrong, you'll get a Pastebin error webpage as the output file instead of your intended script. Also, the Pastebin scripts have not been vetted by us so be sure to inspect all scripts fetched from Pastebin.

### -Remove: Removes a downloaded script
Usage:
BGET -remove script
Example:
BGET -remove test
If “script” is “Pastebin”, it deletes all downloaded Pastebin scripts.

### -Update: Updates the specified script.
Usage:
BGET -update -usemethod script
Supported methods: JS, VBS, PS, CURL, BITS
Example:
BGET -update -usejs test

### -Info: Retrieves basic info about a script.
Usage:
BGET -info -usemethod script
Supported methods: JS, VBS, PS, CURL, BITS
Example:
BGET -info -usevbs test

### -list: Lists either local scripts or scripts on the server.
Usage:
To list local sctipts:
BGET -list -local
To list scripts on the server:
BGET -list -server -usemethod
Example:
BGET -list -server -usejs
Supported methods: JS, VBS, PS, CURL, BITS

### -Upgrade: Updates bget to the latest version
Usage:
BGET -upgrade -usemethod
Example:
BGET -upgrade -usevbs
Supported methods: JS, VBS, PS, CURL, BITS

### -Help: prints the help test.

## Methods
Bget’s  ‘methods’ are the various ways through which Bget interacts with servers.
There are currently 5 methods:
1.	The JS method: It uses a JS download script.
2.	The VBS method: Uses a download script written in VBS.
3.	The PS method: uses Powershell to download resources.
4.	The BITS method: Uses bitsadmin to download resources. It is not compatible with the Pastebin switch.
5.	The CURL method: Uses curl to download resources.
Usage:
BGET [-switch] [-method] [-script]
Where the methods are: -usejs, -usevbs, -useps, -usebits,  -usecurl.
Examples: 
•	BGET -get -usejs test
•	BGET -update -usevbs test
•	BGET -pastebin -useps 1wsBxRs4
•	BGET -list -server -usebits
•	BGET -upgrade -usecurl
•	BGET -info -usejs test

## Contact
If you're having an issue with bget, would like to submit a script or just want to chat, contact us at batchget [at] gmail [dot com]

