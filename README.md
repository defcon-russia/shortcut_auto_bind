# shortcut_auto_bind
Windows LNK/URL shortcut auto-binding hotkey (not a bug, feature)

This is small note about one MS Windows feature, that could be not known to everyone. At least I did not know about it before I did my small research.

Explorer on startup will parse all URL/LNK (PIF... if you are old) and get hot-key value. Then it will be registered with a hook.

![Shortcut](https://defcon-russia.ru/images/hotkey.png)

Of course, you can  add raw hot-key code, so it can be not only "CTRL+ALT+..." but any... for example DEL key or ESC.. or anything.
This is feature, of course, not a bug, but it can be abused by malware guys... so good thing to know.

LNK:
![Edit lnk](https://defcon-russia.ru/images/lnk_2e.png)

URL:
![Shortcut](https://defcon-russia.ru/images/url_46.png)

Explorer.exe on stratup...
![Explorer](https://defcon-russia.ru/images/explorer.png)

Path from where explorer.exe will look shortcuts

* %AppData%\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar .
* %AppData%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts
* %AppData%\Microsoft\Windows\Start Menu
* %UserProfile%\Desktop

PoC:

Copy "Internet Explorer.lnk" to the Desktop, restart PC (or just restart explore.exe), press DEL.

by Alexey Sintsov
