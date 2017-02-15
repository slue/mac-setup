# MySQL

### Install

We will install [MySQL](http://www.mysql.com/) using Homebrew, which will also install some header files needed for MySQL bindings in different programming languages \(MySQL-Python for one\).

To install, run:

```
$ brew update # Always good to do
$ brew install mysql
```

After that we need to secure mysql:

```
$ mysql.server start
$ mysql_secure_installation
$ mysql.server stop
```

### Usage

To have launchd start MySQL now and restart at login:

```
$ brew services start mysql
```

Or, if you don't want/need a background service you can just use the `mysql.server` tool:

```
$ mysql.server start
```

To stop it when you are done, run:

```
$ mysql.server stop
```

You can see the different commands available for `mysql.server` with:

```
$ mysql.server --help
```

To connect with the command-line client, run:

```
$ mysql -uroot
```

\(Use `exit` to quit the MySQL shell.\)

### GUI Tool

It is always nice to have a GUI tool for managing databases. For mac, you can use [SequelPro](http://www.sequelpro.com/) to manage local and remote mysql databases. It is a free tool, you can donate to support the development.

