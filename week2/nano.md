###Week 2: Nano Editor

-----

We have become comfortable navigating our server and creating content with `cd`, `ls`, `mkdir`, `touch`. We've also used `echo "content" > file.txt` to replace text in a file and `echo "content" >> file.txt` to append. Make sure your [permissions have been updated](www-data.md) before moving on.

Being comfortable with these tools is fundamental, but of course there are more powerful methods to edit text in the Terminal. Imagine needing to construct a complex website with just `echo` at our disposal!

Another useful command in Bash is `nano`, which is a very small and simple [hence the name!] text editor.

Let's connect to our server.

```
ssh -i ~/.ssh/identity.pem ubuntu@elasticIPaddress
```

And then, let's move to our web directory.

```
cd /var/www/html
```

Let's create a test text file to edit.

```
touch textfile.txt
```

The `nano` is used like so.

```
nano textfile.txt
```

You should now see a blank text canvas surrounded by a frame of information. At the top of the screen you will see a titlebar.

```
GNU nano 2.5.3              File: textfile.txt
```

Below this, you can type as though your terminal is a barebones word processor.

And at the bottom of the screen, helpful keyboard shortcuts are annotated. The `^` caret character signifies the use of the control modifier key.

```
^G Get Help  ^O Write Out   ^W Where Is   ^K Cut Text     ^J Justify   ^C Cur Pos
^X Exit      ^R Read File   ^\ Replace    ^U Uncut Text   ^T To Spell  ^_ Go To Line
```

Of these shortcuts, only three are regularly used.

```
^O Write Out
```
This command saves your file, after confirmation that the filename is correct.

```
^W Where Is
```
This command finds a text string in the current file.

```
^X Exit
```
Quit `nano`, after a prompt to save any changes.

Use `nano` to make quick changes on your server directly. It is a simple program, without the bells-and-whistles offered by more contemporary text tools. We will install the [Sublime text editor](sublime.md) and connect it to our AWS instance.  
