# FlexibleIEPOS

This directory contains binary and source code for the Flexible I-EPOS project.
The I-EPOS is used in the "Appliance-Level Flexible Scheduling for Socio-Technical Smart Grid Optimisation" paper, as the demand response program.

The directory can be opened as a Intellij Idea project in order to modify and build the code.

Execute the program with
> java -jar tutorial.jar
Note that Oracle Java 8 is required to run the program.

Important files and folders:
tutorial.jar   a simple simulation that can be configured to some extent
src/        contains the source code of the project
lib/        contains all libraries I-EPOS depends on
conf/       this folder contains configuration files for I-EPOS
datasets/   datasets (in format of *.plans) should go here
target/  	the Intellij Idea project files
out/		the output folder for artifacts



#------------------------------------
Replicating the results of the paper
#------------------------------------
In order to execute I-EPOS, the following documentation is necessary:
	http://epos-net.org/software_doc/documentation/index.html
            *to build I-EPOS, you need maven set up.
To run I-EPOS, copy the plan files from the intended experiment to the dataset folder in the I-EPOS directory.
The plans used in the paper are available online at:
https://figshare.com/articles/Flexible_Appliance_Scheduling_Survey_Dataset/8276624
Modify the conf/epos.properties file with the appropriate settings (Table 4)
I-EPOS can be executed by two ways:
	Command line: 
		java –jar epos-tutorial.jar #default config file is used
		java –jar epos-tutorial.jar “path/to/conf” #custom config file
	Source code: in you IDE of choice, build and run the code.
The results will be in the output folder.


*The attached presentation file: "EPOS_tutorial.pdf" provides a summary tutorial on how to use I-EPOS.
