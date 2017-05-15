# SQL2DOX
Created in 2012! 
This project is source code analyser + documentation tool. 
The purpose: analyse PL/SQL source code and based on that code build a documentation.
Using the program:
a) Run SQLAn  -sqldialect:oracle -dSQLML -projectname:your_project your_file.sql - this program creates an ASG graph based on the source code. This is an Columbus software (FrontendArt) 
b) Run Komments your_file.sql which is an utility written by me. Its purpose to extract from source  those comments which have already existed. This is important because the SQLAn does not do that. 
Run SQL2DOX (written by me) reads the ASG and the comments. This software creates an XML from Columbus schema for Doxygen. The program also creates the config file for Doxygen.  
Run iconv utility to convert the XML into UTF-8. 
Run the modified doxygen to show the documentation. Doxygen has used much more element than Columbus so I had to improve its skills. 

Folders:
- SQL2DOX/SQLAPI-28823/Analyzer : The place of Columbus Analyser tool called SQLAn
- SQL2DOX/SQLAPI-28823/doc : the model of PL/SQL ASG
- SQL2DOX/SQLAPI-28823/src/bin/lib/i686-Linux - Columbus libraries
- SQL2DOX/SQLAPI-28823/src/bin/Release/i686-Linux/Columbus - SQL2DOX, Doxygen (modified), Komments binaries
- SQL2DOX/SQLAPI-28823/ext -boost libraries
- SQL2DOX/SQLAPI-28823/trunk - the source code of SQL2DOX (the actual code with main.cpp resides in src/trunk/cl/visitor), the other folder contains header files related to Columbus libraries
- SQL2DOX/SQLAPI-28823/tesztek contains a whole test material including the binaries and tesztelek.sh which is a batch.
- KOMMENTS folder contains the source of the little utility which wxtracts comments from PL/SQL source
- DOC conatins the documentation (written in hungarian)
- DOXYGEN contains the original and the modified version of doxygen 1.8.1 /the documentation contains the list of modified files of doxygen/
