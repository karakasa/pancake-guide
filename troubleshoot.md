# Troubleshoot

## "Load failure" messages pop up when starting Grasshopper

* Pancake requires at least .NET framework 4.5, which is shipped with Rhinoceros 6 but not with Rhino 5. Check the .NET framework downloader [here](https://www.microsoft.com/en-us/download/details.aspx?id=30653).

## No pop-up, but cannot find "Pancake" menu

* Make sure you have .NET framework 4.5 installed
* Check if you can find `Pancake` category in component tab
  * If found, Pancake failed to load the menu. See Contact.
  * Check if all files belong to Pancake is unblocked. Unblock them if not. If it is a new installation, you should at least make sure `Pancake.gha` is unblocked, as it will notify you if other components have any trouble.
    * If problem persists, see Contact.



