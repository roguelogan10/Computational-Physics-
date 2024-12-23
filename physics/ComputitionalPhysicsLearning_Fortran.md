# The Computer

Fortran = Formula Translation

Fortran has been built mainly for numerical applications. Its structure is simple and can be used both
for procedural and object oriented programming.

| Compilers(language that need to be compiled by a compiler) | Interpreters(languages that are interpreted line by line)|
|---|---|
| A compiler is a tool that analyzes the whole program and optimizes the computer instructions executed by the computer. | simple in their use, but they can be prohibitively slow when it comes to a numerically demanding program  |
| Very fast and high performance computing  | if programming time is more valuable, then a simple, interpreted language can lead to faster results|
|Fortran, C, C++ , Java,...| Python, perl, awk,shell scripting, Macsyma, Mathematica, Octave, Matlab,...|


- The shell is a program that “connects” the user to the operating system.  We use a shell to “send” commands to the
operating system, which is the most effective way to perform complicated tasks.


### Operating system

In the Unix operating system everything is a file, and files are organized in a unique and unified filesystem. 


#### filesystem
There is at least one path in the filesystem associated with each file. There
are two types of paths, *relative paths* and *absolute paths*

```
bin/RungeKutta/rk.exe 
/home/george/bin/RungeKutta/rk.exe

```

These two paths refers to the same file. The first one is the *relative path* and the sescond is the *absolute path*. Absolute paths start by a slash / character. 

```
/home/john/bin/RungeKutta/rk.exe
/home/george/CompPhys/bin/RungeKutta/rk.exe

```



These absolute paths refers to differents files because the paths are not the same. 

- '/': is the *root directory*
- directory: position in the filesystem. We are in the *current or working directory*
- Every directory has a unique parent noted by *..*
- The parent of the *root directory* is itself.
- */home* : home directory
- */etc* : configuration files directory
- */bin* or */usr/bin* or */usr/local/bin* : application executables directory
- */lib* or */usr/lib*: software libraries
- '.': Current directory
- '..': Parent directory
- '~' : home directory of the user

![Texte alternatif](https://github.com/roguelogan10/images/blob/main/filesystem.png "Titre de l'image")

the filesystem is a tree of directories with the root directory
at its top which branch to its subdirectories, which in their turn branch
into other subdirectories and so on.


**Basic command for filesystem navigation**



| commands| definition | role | arguments |
|---|---|---|---|
|cd | change directory | change the current directory | absolute/relative path|
| pwd | print working directories| print working directories| No arguments|
| mkdir | Make a directory| creates new directories| the name of the new directory |
|rmdir |removes directories|  removes empty directories| the name of the empty directory|
|mkdir -p|  |create directories more than one level down the filesystem| the new path|  
|ls| list short| list the contents of a directory|No argument/the name of the directory|
|ls -l| list the contents of the current directory together with useful information on the files in 9 columns| No argument/the name of the directory|


The first column lists the permissions of the files (see below). The second one lists the number of links of the files(For a directory,it is the number of its subdirectories plus 2(corresponding to the parent directory
and itself)). The third one lists the user who is the owner of each file. The fourth one lists the group that is assigned to the files. The fifth one lists the size of the file in bytes (=8 bits). The next three ones
list the modification time of the file and the last one the paths of the files.File permissions9 are separated in three classes: owner permissions,
group permissions and other permissions. Each class is given three specific permissions, r=read, w=write and x=execute. For regular files, read
permission effectively means access to the file for reading/copying, write permission means permission to modify the contents of the file and execute permission means permission to execute the file as a command10.
For directories, read permission means that one is able to read the names of the files in the directory (but not make it as current directory with the cd command), write permission means to be able to modify its contents
(i.e. create, delete, and rename files) and execute permission grants permission to access/modify the contents of the files (but not list the names
of the files, this is granted by the read permission).

The command ls -l lists permissions in three groups. The owner (positions 2-4), the group (positions 5-7) and the rest of the world (others-positions 8-10)

File permissions can be modified by using the command `chmod`:
```
> chmod u+x file
> chmod og-w file1 file2
> chmod a+r file

```

Using the first command, the owner (u≡ user) obtains (+) permission to execute (x) the file named file. Using the second one, the rest of
the world (o≡ others) and the group (g≡group) loose (-) the write (w) permission to the files named file1 and file2. Using the third one,
everyone (a≡all) obtain read (r) permission on the file named file.

**Basic command for administering files in the filesystem**

| commands| definition | role | arguments |
|---|---|---|---|
|cp |copy| copies the contents of files into other files| *first file* and *second file*|
|mv | move |moves, or renames, files| filename and the directory where to put the file/ *old name* and *new name*|
|rm | remove| deletes files| name of the file|
|rm -i| remove| asked for confirmation before delete| name of the file|
