#ARM-Cross-Compile-Makefile

This is a Makefile i made that is good for cross compiling or general compiling. If you copy this Makefile, any place you see a tab, delete the tab and re-tab. The tab does not copy over nicely. Tabs are important in a Makefile. Also, some c source files want to use gcc instead of g++. So replace the C compiling with $(GCC) instead of using $(CC). It will compile applications and Shared Libraries.
It assumes includes will be in a folder called “include” and source files will be in a folder called “src”.

###Folder Structure
	Project_Root
		-> src
			-> app.c
			-> main.cpp
		-> include
			-> app.h

###Commands
Here are the commands to use with the Makefile
	make                       // Build Release version ARM
	make BUILD=devel           // Build Debug version ARM
	make BUILD=rel             // Build Release version ARM
	make ARCH=x86              // Build Release version X86
	make BUILD=devel ARCH=x86  // Build Debug version X86
	make clean                 // Clean project
	make doxygen               // Make doxygen files
	make doxygen_clean         // Clean doxygen files