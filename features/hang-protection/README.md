# Hang Protection

{% hint style="info" %}
This feature is unavailable on Mac. See [detailed information](../../miscellaneous/differences-between-windows-and-mac-version.md#hang-protection).
{% endhint %}

Regardless of the autosave setting, Pancake will do an emergency save whenever Grasshopper loses responsiveness for too long. Remember the time when you wired a buggy connection to make Grasshopper hang forever and didn't save your file? That is past.

### How to enable/disable this feature?

* Navigate to "Pancake" menu, check/uncheck "Enable Hang Protection".
* This feature is disabled by default.
* Safe mode will suppress this feature temporarily.

### Where to find the emergency save?

* They are usually stored in the same location of the original document, with a label "_\_PancakeEmergency_".
* If you haven't saved, or the former location is unwritable, or the previous save failed, the emergency save will be put in the temporary directory \(press Windows+R, input **%temp%** and click OK\), starting with "_PancakeEmergency\__".

### How long does Pancake wait before saving?

* The threshold of Pancake recognizing Grasshopper has lost responsiveness is **60-90 seconds** \(as of 1.2.0.0\), or 60-62 seconds in older versions.
* If the system load is extremely high, you may need to wait significantly longer.

### What will be saved?

* Pancake will only save the current Grasshopper document, excluding any other loaded scripts nor the Rhino file.
* Alongside the saved file, Pancake will create a text file, describing [what leads to the problem](how-to-diagnose-a-hang-report.md). For example, you will read messages like `Problem might be caused by Component_PipeSurface in SurfaceComponents`, attached with a [stacktrace](https://en.wikipedia.org/wiki/Stack_trace).
* As of 1.2.0.0, Pancake will save your document correctly when the editor is inside a cluster. Before this version, Pancake will save the cluster instead.

### What else should I also notice?

* Remember to lock the solver before you load the emergency save, because the file is likely to raise another hang.
* Hang is not always a bad thing. If you are running a time-consuming task, switching off Hang Protection will improve the performance.
* This feature applies to hang only. Pancake is powerless to crash. We recommend you to leave AutoSave feature on.
* As of now, Pancake cannot detect hang during plugin initilization, that is, between the time when Grasshopper is launched and the editor window pops up.

### For technical nerds...

* Double-click the Grasshopper canvas and input `#pcRoutineStatus` to see the internal status of HangDetector.

