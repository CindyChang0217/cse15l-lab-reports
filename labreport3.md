**Lab Report 3**

*Command line options for "find"*

* find -name
* find - 
* find -type

>find -name

First example:

Input
```
cindy@DanmengdeMacBook-Air 911report % find . -name 'chapter-1.txt'
```
Output
```
./chapter-1.txt
```
Explanation:
This command line is to find the files named exactly "chapter-1.txt" under the current directory 911report. The result shows that there exists 1 such file. This is useful for finding the specific desired files from a plenty of files under the directory. 

Second example:

Input
```
cindy@DanmengdeMacBook-Air TECHNICAL % find . -name 'chapter*'
```
Output
```
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-3.txt
./911report/chapter-2.txt
./911report/chapter-1.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-9.txt
./911report/chapter-8.txt
./911report/chapter-12.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
```
Explanation: This command find all files whose name contains the key word chapter in the beginning under the directory technical including any subdirectory it contains. This is useful for finding the files containing speicifc keyword from all files. 

Third example:

Input:
```
cindy@DanmengdeMacBook-Air TECHNICAL % find 911report -name '*txt'
```
Output:
```
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```

Explanation:
This command finds all files whose name ends with keyword txt under the directory 911report. This is useful when we want to find all files stored in a certain type under a directory. 

> find -type

First example:

Input
```
cindy@DanmengdeMacBook-Air TECHNICAL % find . -type d
```
Output
```
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```

Explanation: This command finds and lists all the subdirectories under the current directory technical including the directory itself. This command is useful when both files and directories exist under a directory and we want to filter only directory under this directory. 

Second example:

Input
```
cindy@DanmengdeMacBook-Air TECHNICAL % find government -type d
```
Output
```
government
government/About_LSC
government/Env_Prot_Agen
government/Alcohol_Problems
government/Gen_Account_Office
government/Post_Rate_Comm
government/Media
```

Explanation:
This command finds and lists all the subdirectories under the directory government including government itself. This command is useful when we want to find all subdirectories of a given directory, excluding all other files under this directory.  

Third example:

Input
```
cindy@DanmengdeMacBook-Air TECHNICAL % find 911report -type f
```
Output
```
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
Explanation: 
This command finds all the files under the directory 911 report. This command is useful when we want to search only for files under a directory. 

> find - ls

First example:

Input
```
cindy@DanmengdeMacBook-Air TECHNICAL % cd 911report
cindy@DanmengdeMacBook-Air 911report % find chapter-1.txt -ls
```
Output
```
2975826      232 -rwxr-xr-x    1 cindy            staff              118656 Oct 25 21:10 chapter-1.txt
```

Explanation: This command prints the asscoiated statistics of the file chapter-1.txt to the terminal. This command is useful when we want to know the detailed information about certain file.

Second example:

Input
```
cindy@DanmengdeMacBook-Air 911report % find . -ls 
```
Output
```
2975825        0 drwxr-xr-x   19 cindy            staff                 608 Oct 25 21:10 .
2975833      520 -rwxr-xr-x    1 cindy            staff              265912 Oct 25 21:10 ./chapter-13.4.txt
2975834      576 -rwxr-xr-x    1 cindy            staff              290993 Oct 25 21:10 ./chapter-13.5.txt
2975830      176 -rwxr-xr-x    1 cindy            staff               89854 Oct 25 21:10 ./chapter-13.1.txt
2975831      216 -rwxr-xr-x    1 cindy            staff              110568 Oct 25 21:10 ./chapter-13.2.txt
2975832      296 -rwxr-xr-x    1 cindy            staff              150467 Oct 25 21:10 ./chapter-13.3.txt
2975836      520 -rwxr-xr-x    1 cindy            staff              264360 Oct 25 21:10 ./chapter-3.txt
2975835      160 -rwxr-xr-x    1 cindy            staff               79803 Oct 25 21:10 ./chapter-2.txt
2975826      232 -rwxr-xr-x    1 cindy            staff              118656 Oct 25 21:10 ./chapter-1.txt
2975837      200 -rwxr-xr-x    1 cindy            staff               99008 Oct 25 21:10 ./chapter-5.txt
2975838      296 -rwxr-xr-x    1 cindy            staff              149063 Oct 25 21:10 ./chapter-6.txt
2975839      256 -rwxr-xr-x    1 cindy            staff              128370 Oct 25 21:10 ./chapter-7.txt
2975841      296 -rwxr-xr-x    1 cindy            staff              149644 Oct 25 21:10 ./chapter-9.txt
2975840      168 -rwxr-xr-x    1 cindy            staff               84835 Oct 25 21:10 ./chapter-8.txt
2975842       24 -rwxr-xr-x    1 cindy            staff                9332 Oct 25 21:10 ./preface.txt
2975829      256 -rwxr-xr-x    1 cindy            staff              127587 Oct 25 21:10 ./chapter-12.txt
2975827       96 -rwxr-xr-x    1 cindy            staff               47307 Oct 25 21:10 ./chapter-10.txt
2975828      144 -rwxr-xr-x    1 cindy            staff               71151 Oct 25 21:10 ./chapter-11.txt
```
Explanation: This command prints the relevant information of all files in 911report directory and the directory itself to the terminal. This command is useful when we want to know the information of all files in current directory. 

Third example:

Input
```
cindy@DanmengdeMacBook-Air technical % find government/Alcohol_problems  -ls
```
Output
```
2976700        0 drwxr-xr-x    6 cindy            staff                 192 Oct 25 21:10 government/Alcohol_problems
2976702       72 -rwxr-xr-x    1 cindy            staff               35927 Oct 25 21:10 government/Alcohol_problems/Session2-PDF.txt
2976703      192 -rwxr-xr-x    1 cindy            staff               94212 Oct 25 21:10 government/Alcohol_problems/Session3-PDF.txt
2976701       64 -rwxr-xr-x    1 cindy            staff               31843 Oct 25 21:10 government/Alcohol_problems/DraftRecom-PDF.txt
2976704      160 -rwxr-xr-x    1 cindy            staff               80034 Oct 25 21:10 government/Alcohol_problems/Session4-PDF.txt
```
Explanation: This command prints the statistics of all the files under the directory Alcohol_problems and the directory itself. This command is useful when we want to find the information of all files and the given directory. 