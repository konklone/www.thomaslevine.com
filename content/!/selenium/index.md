---
title: Installing Selenium
created_at: 2012-04-24
kind: article
tags: ['data']
---

The Selenium Server documentation is unnecessarily painful;
installing Selenium is not hard.

Set up a real framebuffer or a
[virtual framebuffer](http://dionysus.uraganov.net/software/how-to-install-selenium-server-with-firefox-on-ubuntu-11-10/)

Download the selenium **standalone** version.

    wget http://selenium.googlecode.com/files/selenium-server-standalone-2.21.0.jar

Run it.

    # If you're using a virtual framebuffer, start it like so
    Xvfb :99 -ac &
    export DISPLAY=:99seleniumrc
    
    java -jar selenium-server-standalone-2.21.0.jar -port 4443

Set that up as a daemon if you wish.

I always have problems with the Chrome driver, but
the Firefox driver has always been fine for me.
