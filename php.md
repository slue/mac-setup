# PHP 7

```
brew tap homebrew/dupes
brew tap homebrew/versions
brew tap homebrew/homebrew-php
brew install php71
```

Check if php-fpm is running:

```
ps aux | grep php-fpm
```

Restart php 7.0

```
brew services restart php71
```

### XDebug

To install XDebug:

```
brew install php71-xdebug
```

Then open the `/usr/local/etc/php/7.1/conf.d/ext-debug.ini` and append the following line:

```
xdebug.remote_enable=1
```

After that restart php \(see above\)

### PHP 7 konfigurieren

Die Datei \`/etc/apache2/other/php7-fpm.conf\` mit folgendem Inhalt erstellen:

```
<IfModule mod_proxy_fcgi.c>
    <FilesMatch \.php$>
        # 2.4.10+ can proxy to unix socket
        SetHandler "proxy:unix:/tmp/php7-fpm.sock|fcgi://localhost/"

        # Else we can just use a tcp socket:
        # SetHandler "proxy:fcgi://127.0.0.1:9000"
    </FilesMatch>


    <IfModule mod_dir.c>
        DirectoryIndex index.html index.php
    </IfModule>
</IfModule>
```

In der Datei \`/usr/local/etc/php/7.0/php-fpm.d/www.conf\` folgende Zeilen ändern:

* \`listen = 127.0.0.1:9000\`

* * wird zu: \`listen = /tmp/php7-fpm.sock\`
* \`user = \_www\`

* * wird zu: \`user = \[DEIN\_USER\]\`

Dann Apache und PHP-FPM neu starten und los gehts …

### Set Interpreter in phpStorm

Executable can be found under `/usr/local/opt/php70/bin/php`

# Apache

Konfiguriere `/etc/apache2/httpd.conf`:

* Aktiviere Module:
  * mod\_proxy
  * mod\_proxy\_\_\_fcgi
  * php5\_module
  * rewrite\_module
* User auf selben von php 7 ändern

### vHosts

Instead of the default configuration to put all vHosts in a single File `httpd-vhost.conf`, configure Apache to use a folder for vHosts:

In `/etc/apache2/httpd.conf` append the 3rd line:

```
# Virtual hosts
#Include /private/etc/apache2/extra/httpd-vhosts.conf
Include /private/etc/apache2/vhosts/*.conf
```



