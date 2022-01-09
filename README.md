# Int_Sec_21-22_Gr15# ELF Parser
 
## Faqja e internetit 
www.elfparser.com 
 
## ELF
ELF qëndron për Executable and Linkable Format. Paraqet strukturën që ndjek file-i binar në sisteme operative si Linux, Solaris, Unix apo sisteme të ngjashme me Unix që i përkasin procesorëve x86. Për dallim nga ELF, Windows përdor formatin PE (Portable Execution), ndërsa machOS përdor mach-o.
Kur shkruhet source code në gjuhë të lartë programuese, nevojitet një compiler për ta përkthyer në object code, që më pas përkthehet në binary code, me ç’rast edhe lidhet me libraritë referencuese. Kjo përmbajtje binare përmban instruksionet machine code të cilat i kupton dhe i ekzekuton CPU në momentin që një compiled file është running.
 
Një ELF file përbëhet nga dy pjesë:
ELF Header – strukturë që përmban metadata për file.

File data – Program header table, Section header table dhe data të referuara nga hyrjet e dy tabelave të lartpërmendura.


![fig](https://user-images.githubusercontent.com/75095476/148683535-0ad0246d-3b6b-4546-b481-07bd4aebd1f0.png)
## Parsing
ELF Parser kategorizon aftësitë e binarit duke miratuar funksionet dhe nënshkrimet e njohura dhe përpiqet të identifikoj malware të njohur si Kaiten, Elfknot dhe BillGates.
 
## Si mund ta compile file-in?
ELF Parser mund të bëhet compile në Windows, OS X ose Linux (demangle dhe testet e njësisë nuk funksionojnë në Windows). Windows përdor projektin VS 2010 në direktoriumin bazë për përpilim ndërsa Linux/OS X përdor CMake.
Compiling në Linux shkon kështu:
 
cd ~/elfparser
mkdir build
cd build/
cmake ..
make
Boost është i domosdoshëm.
 
## Përdorimi i CLI
Përdoruesi mund të kalojë në një skedar të vetëm (-f) ose një direktorium (-d) skedarësh: 
 
./elfparser-cli --help

options:

  --help                  -A list of command line options
  
  --version               -Display version information
  
  -f [ --file ] arg       -The ELF file to examine
  
  -d [ --directory ] arg  -The directory to look through.
  
  -r [ --reasons ]        -Print the scoring reasons
  
  -c [ --capabilities ]   -Print the files observed capabilities
  
  -p [ --print ]          -Print the ELF files various parsed structures.
 
## Licensa burimore
GPLv3. Shihni dosjen LICENSE. 

