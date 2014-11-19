---
layout: page
title: LaTeX Setup
excerpt: "Installation instructions"
modified: 2014-11-09T15:14:14
---

* Table of Contents
{:toc}

# Online LaTeX editors

## writeLaTex: 

	<https://writelatex.com>

## ShareLaTeX:

	<https://www.sharelatex.com/>

# Windows OS

## TeXdistribtion

### TeXLive (Recommended)

1.  Download the TeXLive ISO ($$\sim 2.5$$ GB) from
    <http://anorien.csc.warwick.ac.uk/mirrors/CTAN/systems/texlive/Images/texlive2014.iso>

2.  Download WinCDEmu (if you don’t have a virtual drive) from
    <http://wincdemu.sysprogs.org/download/WinCDEmu-3.6.exe>

3.  To install Windows CD Emulator follow the instructions at
    <http://wincdemu.sysprogs.org/tutorials/install/>

4.  Right click the iso and mount it using the WinCDEmu as shown in
    <http://wincdemu.sysprogs.org/tutorials/mount/>

5.  Open your virtual drive and run `setup.pl`

### MikTeX

1.  Download Basic-MikTex 2.9 (32bit or 64bit) from
    <http://miktex.org/download>

2.  Run the installer <http://docs.miktex.org/2.9/manual/ch02s02.html>

3.  To add a new package go to Start \>\> All Programs \>\> MikTex 2.9
    \>\> Maintenance (Admin) and choose Package Manager

4.  Select or search for packages to install


## TexStudio (TeXEditor)

1.  Download TexStudio 2.8 from
    <http://texstudio.sourceforge.net/#downloads>

2.  Run the installer

# Mac OS X

## MacTex 2014

1.  Download the file from
    <http://mirror.ctan.org/systems/mac/mactex/MacTeX.pkg>

2.  Extract and double click to run the installer. It does the entire
    configuration, sit back and relax.

## TexStudio (TeXEditor)

1.  Download TeXStudio 2.8 from
    <http://texstudio.sourceforge.net/#downloads>

2.  Extract and Start

# Unix/Linux

## Installation using Linux packages

### Fedora/RedHat/CentOS: 

``` 
sudo yum install texlive 
sudo yum install psutils 
```

### SUSE:

``` 
sudo zypper install texlive
```

### Debian/Ubuntu:

```
sudo apt-get install texlive texlive-latex-extra 
sudo apt-get install psutils
```

## Direct installation (latest version) 

### Getting the distribution

1.  TeXLive can be downloaded from
    <https://www.tug.org/texlive/acquire.html>. You might require wget
    to download through proxies.

2.  TeXLive is provided by most operating system you can use (rpm,
    apt-get or yum) to get TeXLive distributions (note: usually it’s the
    old TeXLive)

### Installation

1.  Mount the ISO file in the mnt directory
    
    ```
    mount -t iso9660 -o ro,loop,noauto /your/texlive2014.iso /mnt
    ``` 

2.  Get wget on your OS (use rpm, apt-get or yum install)

3.  Run the installer script install-tl.

    ```
    cd /your/download/directory
    ./install-tl
    ```

4.  Enter command ‘i’ for installation

5.  Post-Installation configuration (Environment variables for Unix):
    <http://www.tug.org/texlive/doc/texlive-en/texlive-en.html#x1-320003.4.1>

6.  Set the path for the directory of TeXLive binaries in your
    `~/.bashrc` file:

    #### 64Bit

        PATH=/usr/local/texlive/2014/bin/x86_64-linux:$PATH; export PATH
        MANPATH=/usr/local/texlive/2014/texmf/doc/man:$MANPATH; export MANPATH 
        INFOPATH=/usr/local/texlive/2014/texmf/doc/info:$INFOPATH; export INFOPATH

    #### 32Bit

        PATH=/usr/local/texlive/2014/bin/i386-linux:$PATH; export PATH 
        MANPATH=/usr/local/texlive/2014/texmf/doc/man:$MANPATH; export MANPATH 
        INFOPATH=/usr/local/texlive/2014/texmf/doc/info:$INFOPATH; export INFOPATH

[^1]: kks32@cam.ac.uk
