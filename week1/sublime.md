###Week 2: Sublime Text

-----

[Nano](nano.md) is a great example of the Unix tool philosophy, which encourages small applications that do one thing really well. But, since it doesn't have syntax highlighting and other useful coding aids, we should explore some alternate text editing tools.

Sublime Text is a highly recommended commercial text editing application, and its package ecosystem offers all kinds of useful add-ons including SFTP support, which we will now setup.

First download, install, and launch [Sublime Text](http://sublimetext.com).

Then, press `control/command+shift+p` to bring up the command palette. Type in `install` and select `Package Control: Install Package`.

After a short delay [look at the bottom of the screen to see the progress], you will be able to search available plugin packages. Type in and select `SFTP` to install it.

`SFTP`, the [Secure File Transfer Prototol](http://www.computerhope.com/unix/sftp.htm), is another terminal command that allows the secure transfer of files from one machine to another.

```
sftp -i .ssh/identity.pem ubuntu@elasticIPaddress
```

It is a very powerful tool, but we will not be using it directly. Instead, Sublime will manage SFTP for us.

Press `control/command+shift+p` to bring up the command palette. There, type in `Browse Server`, select it, and then `Add a New Server`.

A new tab will open with default server setup content.

```
{
    // The tab key will cycle through the settings when first created
    // Visit http://wbond.net/sublime_packages/sftp/settings for help
    
    // sftp, ftp or ftps
    "type": "sftp",

    "sync_down_on_open": true,
    "sync_same_age": true,
    
    "host": "example.com",
    "user": "username",
    //"password": "password",
    //"port": "22",
    
    "remote_path": "/example/path/",
    //"file_permissions": "664",
    //"dir_permissions": "775",
    
    //"extra_list_connections": 0,

    "connect_timeout": 30,
    //"keepalive": 120,
    //"ftp_passive_mode": true,
    //"ftp_obey_passive_host": false,
    //"ssh_key_file": "~/.ssh/id_rsa",
    //"sftp_flags": ["-F", "/path/to/ssh_config"],
    
    //"preserve_modification_times": false,
    //"remote_time_offset_in_hours": 0,
    //"remote_encoding": "utf-8",
    //"remote_locale": "C",
    //"allow_config_upload": false,
}
```

Replace `example.com` with your elastic IP address or purchased domain name next to `host` inside of quotation marks and replace `username` with `ubuntu` in the same way.

```
    "host": "35.166.246.200",
    "user": "ubuntu",
```    

Set the `"remote_path"` to `/var/www/html`.

```
    "remote_path": "/var/www/html",
```

Set the `"ssh_key_file"` to the path to your identity file.

```
//"ssh_key_file": "~/.ssh/identity.pem",
```

Also, remove the `//` at the beginning of this line, and add the path to your .pem identity file.

```
//"ssh_key_file": "~/.ssh/id_rsa",
```

Save this file after these four edits with a recognizable name inside of the default save location (a hidden `sftp_servers` directory).

After saving this file, you can `control/command+shift+p` to bring up the command palette. There, type in `Browse Server`, select it, and then select your filename. This will then allow you to browse the Apache server directory on your AWS server, and easily edit files! 

You can manipulate files and directories from the command palette. Selecting `Edit` will allow you to edit any file on your remote server. Saving the file in Sublime will upload your changes to the server. Convenient!

Now, let's move onto [creating html content](block.md) on the server.
