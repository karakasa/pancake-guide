# File Block Monitor

{% hint style="info" %}
This feature is unavailable on Mac as macos doesn't have similar mechanism.
{% endhint %}

Some libraries and their dependencies need to be unblocked in "File Properties" dialog to make effect. It can be annoying when there are a lot of files, or some plugin doesn't show up when you forget to do that. File block monitor will pop up when libraries are blocked.

### How to enable/disable this feature?

* Navigate to "Pancake" menu, check/uncheck "Enable File Block Monitor".
* This feature is **disabled** by default.
* Safe mode will suppress this feature temporarily.

### Why can't Pancake just unblock them without asking me?

* It is all about security. The default behavior of Pancake should not enlarge [attack surface](https://en.wikipedia.org/wiki/Attack_surface) of Rhinoceros and Grasshopper.
* You can override the security measure by clicking "Always unblock" in the pop-up window.
* You will receive notification again if you turn off and on File Block Monitor.
* You will always see a report window of what are unblocked afterwards, even if you turn on Automatic Unblock.

### What are the meanings of description in pop-up window?

* COFF loaded
  * The current loading mechanism of Grasshopper ignores the block on this library. It is recommended to unblock the file, in case that the library is referenced by others.
* Not loaded
  * The file is not loaded due to the block. The file is usually a related assembly. You need to unblock it to make some libraries work.
* Native DLL
  * Rare. The file might be a dependency of another library. You need to unblock it to make some libraries work. It is also possible that the plugin is encrypted and Pancake cannot determine what it should be.

### What else should I also notice?

* Pancake will try to load the unblocked libraries but cannot guarantee success. It is recommended to restart Grasshopper / Rhinoceros if you unblocked something.
* If enabled, the monitor will notify you everytime new plugins are installed.



