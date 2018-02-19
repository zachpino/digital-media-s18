###Week 2: Permissions Improvement

-----

Our server as setup last week requires us to use `sudo` to create and edit files on the server, since the `ubuntu` user does not by default have write access to the `/var/www/html` directory. 


```
ssh -i ~/.ssh/identity.pem ubuntu@elasticIPaddress
```
Connect to the server.

```
sudo adduser ubuntu www-data
```
The apache web server uses the www-data group to manage who can edit served files. This line adds the `ubuntu` user to that group.

```
sudo chown -R www-data:www-data /var/www
```
This line ensures that the www-data group owns the /var/www folder, so that our new group membership applies to all subfolders of `/var/www`.

```
sudo chmod -R g+rwX /var/www
```
Change permissions on the directory. We are `R`ecursively adding`+` to the www-data `g`roup of our current user `r`ead,`w`rite, and e`X`ecute permissions. Read more about how chmod works by running  `man chown`. 

```
exit
```
Disconnect from the server for these changes to take effect.

Let's reconnect to our server to test.

```
ssh -i ~/.ssh/identity.pem ubuntu@elasticIPaddress
```

And then, let's move to our web directory.

```
cd /var/www/html
```

Try this, it should work!

```
echo "permissions problems solved"  > test.html
```

Visit your `[elastic IP address]/test.html` to check if your server is behaving.

Let's now work through some other methods for [editing text](nano.md) on our server.
