# shortcut_auto_bind
Windows LNK/URL shortcut auto-binding hotkey (not a bug, feature)

This is a small note about one MS Windows feature, that could be not known to everyone. At least I did not know about it before I did this small research.

Explorer on startup will parse all URL/LNK files (PIF... if you are old) and get hot-key value. Then it will be registered with a hook.

![Shortcut](https://defcon-russia.ru/images/hotkey.png)

Of course, you can  add raw value of hot-key code, so it can bypass windows limitation ("CTRL+ALT+..." only), and with this simple trick you can register, for example, DEL key or ESC.. or almost anything.

This is a feature, of course, not a bug, but it can be abused by malware guys (as autorun by trigger)... so good thing to know.

LNK:
![Edit lnk](https://defcon-russia.ru/images/lnk_2e.png)

URL:
![Shortcut](https://defcon-russia.ru/images/url_46.png)

Explorer.exe on stratup...
![Explorer](https://defcon-russia.ru/images/explorer.png)

Path from where explorer.exe will search for shortcuts

* %AppData%\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar .
* %AppData%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts
* %AppData%\Microsoft\Windows\Start Menu
* %UserProfile%\Desktop

PoC:

Copy "Internet Explorer.lnk" to the Desktop, restart PC (or just restart explore.exe), press DEL.
