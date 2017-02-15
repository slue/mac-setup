# Homebrew

Package managers make it so much easier to install and update applications \(for Operating Systems\) or libraries \(for programming languages\). The most popular one for OS X is [Homebrew](http://brew.sh/).

### Install

An important dependency before Homebrew can work is the **Command Line Tools** for **Xcode**. These include compilers that will allow you to build things from source.

We can install Hombrew! In the terminal paste the following line \(without the `$`\), hit **Enter**, and follow the steps on the screen:

```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Open an new terminal tab with **Cmd+T** \(you should also close the old one\), then run the following command to make sure everything works:

```
$ brew doctor
```



