# ClusterHat_Distribute
Command line program for use with the Raspberry Pi cluster hat to distribute copies of the program from the controller to all Pi Zeros.


##Usage: distribute [OPTION]... [FILE]...
Program to distribute given files to all Raspberry Pi Zeros connected to the controller board. Will create directories on the
controller board if they do not already exist.
* -p, --power 	Turn on Zeros, default assumes zeros are already on
* -n, --number: 	Distribute to given number of zeros only, if used in conjunction with -o, that many Zeros will be turned on. Default is 4.
* -o, --output: 	Path to distribute to, defaults to current path
* -h, --help: 	Display the help text
* -v, --verbose: 	Descriptive output

##Examples:
* distribute my_program.py	Attempts to copy my_program.py to all Pi Zero's
   
* distribute -n 3 -p my_program.py another_program.py		Will turn on 3 
		Pi Zeros before attempting to copy both files to the 3 Pi Zeros
* distribute -o /home/pi/example/ my_program.py	Attempts to copy file in 
		local current working directory to Pi Zeros directories /home/pi/example/my_program.py 

_Requires python3 to run._
