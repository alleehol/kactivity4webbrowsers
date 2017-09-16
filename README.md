# kactivity4webbrowsers

Web browser scripts for minimal support of KDE activities.


## chrome-browser-ka

Wrapper script for chromium. Assumptions (valid at least for \*ubuntu)

        program: /usr/bin/chromium-brower
        starter: /usr/share/applications/chromium-browser.desktop
        config:  ~/.config/     
        

Installation
------------

```shell
git clone https://github.com/alleehol/kactivity4webbrowsers.git

# Either per user: Make sure `~/bin` exits and is in front of `/usr/bin` in the PATH
ln -s /path/to/kactivity4webbrowsers/chromium-browser-ka ~/bin/chromium-browser

 # or system wide: Make sure `/usr/local/bin` exits and is in front of `/usr/bin` in the PATH
 sudo ln -s   /path/to/kactivity4webbrowsers/chromium-browser-ka /usr/local/bin/chromium-browser
```


Features
--------

* independent settings and restore per activity
* Allows to configure default browser config
* script and starter still work with renamed activities

Limitations
-----------

* assigning to more than one activity does not work as expected
   (restore only when original activity is started)

* removing an activity does not cleanup the corresponding browser data

* Firefox support is not up to date and mostly untested
         
         
# Ideas for enhancements

1. **Chromium never used before our wrapper**
...In this case no ~/.config/chromium exists, that can be copied.


* **Huge ~/.config/chromium/**
  * Problem: An fresh chome-browser uses ~ 22 MB.  Mine grew to 290 MB.
  * Task: find a way to strip unnecessary data when duplicating ~/.config/chrome/

    When we don't duplicate but create it, the kwallet folder used is different. (I want it to be the same).

* **Support other Browsers**
  * Chrome should be easy
  * Firefox is a bit different

