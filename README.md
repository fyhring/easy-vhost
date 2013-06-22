# Easy-vhost

A terminal program for creating vhosts.
Tested on Mac Mountain Lion and Windows 7 with xampp & wamp.

### Usage:
To add a vhost:
```
> sudo php vhost -n "helloworld.dev" -p "path/to/hello/world/public"
```
To delete a vhost:
```
> sudo php vhost -d "helloworld.dev"
```

### Setup
You need to set the app up before using it. To do that you need to find your apache folder and your localhost www folder.

**Windows:**
```
> php vhost -setup
Is your OS Windows? Please type 'yes' or 'no' (default is no): > yes
What is the path to the version of apache you're using: > C:\wamp\bin\apache\apache2.2.22
What's your localhost www/public_html folder? > C:\wamp\www

The setup is now finish.
```
Unfortunately on Windows you have to add this line at the very end of your **httpd.conf** file.
```
Include "C:\wamp\bin\apache\apache2.2.22\other\*.conf"
```

**Mac OS X**
```
> sudo php vhost -setup
Is your OS Windows? Please type 'yes' or 'no' (default is no): > no (or just hit enter)
What's your localhost www/public_html folder? > /Library/WebServer/Documents

The setup is now finish.
```

It should be this easy, if you're having any trouble please let me know.

If it doesn't work on Mac, check your httpd.conf file, at the very end it should contain this line:
```
Include /private/etc/apache2/other/*.conf
```
