Virtualhost Manage Script
===========

Bash Script to allow create or delete apache/nginx virtual hosts on Ubuntu on a quick way.
It allows you to create a vhost.conf for laravel by setting the `/public`-directory within the vhost_dir/ app_dir as the document-root. 

## Installation ##

1. Download the script
2. Apply permission to execute:

```
$ chmod +x /path/to/virtualhost.sh
```

3. Optional: if you want to use the script globally, then you need to copy the file to your /usr/local/bin directory, is better
if you copy it without the .sh extension:

```bash
$ sudo cp /path/to/virtualhost.sh /usr/local/bin/virtualhost
```

### For Global Shortcut ###

```bash
$ cd /usr/local/bin
$ wget -O virtualhost https://raw.githubusercontent.com/RoverWire/virtualhost/master/virtualhost.sh
$ chmod +x virtualhost
$ wget -O virtualhost-nginx https://raw.githubusercontent.com/RoverWire/virtualhost/master/virtualhost-nginx.sh
$ chmod +x virtualhost-nginx
```

## Usage ##

Basic command line syntax:

```bash
$ sudo sh /path/to/virtualhost.sh [create | delete] [domain] [optional root_dir]
```

With script installed on /usr/local/bin

```bash
$ sudo virtualhost [create | delete] [domain] [optional root_dir]
```

### Examples ###

to create a new virtual host under /var/www/mysite.dev:

```bash
$ sudo virtualhost create mysite.dev
```
to create a new virtual host with deeper root-dir /var/www/anothersite.dev/my_dir:

```bash
$ sudo virtualhost create anothersite.dev my_dir
```
to delete a virtual host

```bash
$ sudo virtualhost delete mysite.dev
```

### Localization

For Apache:

```bash
$ sudo cp /path/to/locale/<language>/virtualhost.mo /usr/share/locale/<language>/LC_MESSAGES/
```

For NGINX:

```bash
$ sudo cp /path/to/locale/<language>/virtualhost-nginx.mo /usr/share/locale/<language>/LC_MESSAGES/
```
