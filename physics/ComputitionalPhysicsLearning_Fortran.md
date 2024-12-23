# The Computer

Fortran = Formula Translation

Fortran has been built mainly for numerical applications. Its structure is simple and can be used both
for procedural and object oriented programming.

| Compilers(language that need to be compiled by a compiler) | Interpreters(languages that are interpreted line by line)|
|---|---|
|   A compiler is a tool that analyzes the whole program and optimizes the computer instructions executed by the computer. | simple in their use, but they can be prohibitively slow when it comes to a numerically demanding program  |
|   | if programming time is more valuable, then a simple, interpreted language can lead to faster results|
|Fortran, C, C++ , Java,...| Python, perl, awk,shell scripting, Macsyma, Mathematica, Octave, Matlab,...|


- The shell is a program that “connects” the user to the operating system.  We use a shell to “send” commands to the
operating system, which is the most effective way to perform complicated tasks.


### Operating system

In the Unix operating system everything is a file, and files are or-
ganized in a unique and unified filesystem. 


#### filesystem
There is at least one path in the filesystem associated with each file. There
are two types of paths, *relative paths* and *absolute paths*

```bin/RungeKutta/rk.exe``` 

```/home/george/bin/RungeKutta/rk.exe```

These two paths refers to the same file. The first one is the *relative path* and the sescond is the *absolute path*. Absolute paths start by a slash / character. 

```/home/john/bin/RungeKutta/rk.exe```

```/home/george/CompPhys/bin/RungeKutta/rk.exe```



These absolute paths refers to differents files because the paths are not the same. 

- /: is the *root directory*
- directory: position in the filesystem. We are in the *current or working directory*
- Every directory has a unique parent noted by *..*
- The parent of the *root directory* is itself.


![Texte alternatif](https://github.com/roguelogan10/images/blob/main/filesystem.png "Titre de l'image")

the filesystem is a tree of directories with the root directory
at its top which branch to its subdirectories, which in their turn branch
into other subdirectories and so on