###Week 1: Accessing the Server

-----

Use the `ssh` command to connect to your AWS server with your [prepared identity file](identityfile.md). AWS uses identity files for verifying identities, so you will need to have a .pem access file setup with `400` permissions. Read about `ssh` and its available options and syntax with  `man ssh`. Use the `-i` option to use your prepared identity file as authentication. You will also need the IP address created in the Elastic IP AWS interface.

First, move to your home folder.

`cd ~`

The `ssh` syntax here involves several parts prepared so far.

`ssh -i path/to/pem/file user@ipaddress`

The defauly username for Ubuntu Linux is `ubuntu`. The command will look something like this when complete.

`ssh -i .ssh/proto_class.pem ubuntu@35.166.246.200`

A warning will open about the authenticity of the host. This is only occuring since its the first time this server is accessed. Type `yes`.

After a short delay, introduction text shows up along with a new prompt. Your terminal is now controlling a computer somewhere else in the world!

`ubuntu@ip-172-31-2-29:~$`

-----

You can easily disconnect from your server as well.

`exit`

You should now be back on your own machine. Pressing the `up arrow` on your keyboard will bring back the last command you used *on your machine*, which should be your `ssh` command for reconnecting.

-----

We can now move on to [setting up software](lampinstall.md) on the server.
