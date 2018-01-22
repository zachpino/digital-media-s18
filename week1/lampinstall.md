###Week 1: Installing Server Software

-----

Now, with [terminal access to the server](serveraccess.md), it is important to do some basic configuration.

The `sudo` command will be used frequently from here on. `sudo` abbreviated from 'substitute user and do,' elevates your terminal so that your command can access files beyond your user account. This is necessary, as the following steps change system-level files on your server.

`sudo passwd` allows you to establish a password. Make it memorable! Note that, when you type in your password, Ubuntu won't show you it. You will then be able to use that password for system-level administration. This will be called your *terminal password* going forward.

`sudo apt-get update` will update all of your Linux system files to their most up-to-date versions. `apt-get` is Ubuntu's package manager, similar to Software Update on macOS and Windows Update on Windows. After a short moment, everything will be updated and installed.

-----

Now that the server machine is a bit more secure and up-to-date, software for serving an HTTP page can now be installed.

`sudo apt-get install lamp-server^`

Type `y` when prompted to begin the installation. At various points, you will be asked to create a password for MySQL. This password going forward will be called your *database password*.

This single line above will install everything we need to serve a website. LAMP is an initialism for Linux, Apache, MySQL, and PHP. These four technologies are fundamental to the web, and are as universal as they are ancient.

- The Linux open source operating system is the foundation of our server, we are using the Ubuntu flavor.
- Apache is the actual web server software, which manages requests and transfers data to and from web browsers.
- MySQL is database software, often used to manage complex structured data from content management systems.
- PHP is a computer language that runs on a server and processes information submitted to Apache from web browsers.

All of these will find a use over the coming weeks.

-----

If you now put your server's IP address into your web browser, you should see the Apache welcome. Our web server is now serving a website. [Pages can now be added](addpage.md) and served to the world.

