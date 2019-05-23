# Version Watermark

It is important to keep version record in a team setting. Pancake provides a easier way of tracking how the script develops.

### How to enable/disable this feature?

* Navigate to "Pancake" menu, check/uncheck "Enable Version Watermark in GH / Rhino".
* This feature is **per file**, and disabled by default.
* "Per file" means the feature is automatically turned on if previous version information exists in the document. And you cannot switch this feature globally.

### What behavior is tracked?

* For Grasshopper script, Pancake records events when somebody who creates, opens and modifies the document. Open event is not recorded if the user doesn't change anything.
* For Rhinoceros document, Pancake records events when somebody creates, opens and saves the document.

### What about my privacy?

* The only included personal information is the author name. First, Pancake uses the name you define in Grasshopper. If that is unavailable, Pancake picks the machine name of your computer instead. If the latter is still unavailable, the author name will be `N/A`.
* You can always click "Remove version watermark in GH / Rhino" to remove all watermarks in the document. This is irreversible.
* **Remember to remove the watermark before publishing your file.**

### Where to find the version report?

* Navigate to "Pancake" menu, click "Show version history..."
* Version report of Grasshopper or/and Rhinoceros are included

### What else should I also notice?

* Modification events from the same author are always merged, so there will be only one latest entry.
* Due to limitation, Pancake only tracks Rhino fiile events when Grasshopper is loaded. We are considering about releasing a stand-alone Rhino plugin that doesn't require Grasshopper.
* The watermark is not bullet-proof. Non-Pancake users can remove them easily. So make sure each of your team member has Pancake on their computer \(Sorry!\).
* However, if Pancake is installed, it has the ability to sustain information in case of an accidental removal.

