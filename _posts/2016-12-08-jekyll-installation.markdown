---
layout: post
title:  "Installing Jekyll via Bash on Ubuntu on Windows 10"
date:   2016-12-08 15:38:37 -0500
categories: jekyll
---

Here's what worked for me.  

### Ruby 

##### *from [Dave Rupert][daverupert]*  

```console
$ sudo apt-add-repository ppa:brightbox/ruby-ng  
$ sudo apt update  
$ sudo apt install ruby2.3 ruby2.3-dev ruby-switch  
$ ruby -v  
``` 

### Python 2.7.12  

##### *from [tecadmin]*  

```console
$ sudo apt-get install build-essential checkinstall  
$ sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev  
$ cd /usr/src  
$ sudo wget https://www.python.org/ftp/python/2.7.12/Python-2.7.12.tgz  
$ sudo tar -xzf Python-2.7.12.tgz  
$ cd Python-2.7.12  
$ sudo ./configure  
$ sudo make altinstall  
```

### Jekyll  

##### *from [Jekyll][jekyllrb]*  

```console
$ sudo gem install jekyll  
$ sudo gem install jekyll bundler  
$ sudo gem install minima  
$ sudo gem install jekyll-feed  
$ cd /mnt/d/git/grishagin.github.io  
$ jekyll new .  
```

### Run

```console
$ jekyll serve
```

After that, navigate to [http://localhost:4000/][localhost] in your browser.

### General Notes

* For bash formatting, \`\`\`*console* works much better than \`\`\`*bash*.
* Command ```jekyll serve``` used to require a ```--no-watch``` option when run in a linux subsystem on Windows (i.e. every content alteration would require re-serving). As of Nov 2017, this is no longer the case.



[daverupert]: http://daverupert.com/2016/04/jekyll-on-windows-with-console/
[tecadmin]: http://tecadmin.net/install-python-2-7-on-ubuntu-and-linuxmint/
[jekyllrb]: https://jekyllrb.com/docs/quickstart/
[localhost]: http://localhost:4000/