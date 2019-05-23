# Downgrade Components \(Rhino 5\)

{% hint style="info" %}
The document applies to Rhino 5 only. If you are using Rhino 6, please read [this version](./).
{% endhint %}

The Grasshopper shipped with Rhinoceros 6 introduces a bunch of new components, some replacing the most basic ones. This feature provides an one-click solution for downgrading them, so that it can be loaded by a Rhino 5 user. **This feature will work without Rhino 6.**

### How to use this feature?

* Navigate to "Pancake" menu, click "Downgrade external script"
* Open an external Grasshopper file

### Which component will be downgraded?

* Subtraction \(with 2 inputs\)
* Multiplication \(with 2 inputs\)
* Evaluate Surface
* Interpolate Curve \(Tangent\)
* Relay component

### What are the possible results?

* Pancake encounters error when downgrading your file
  * Grasshopper script may be corrupt
  * Please contact us with the script file.
* Pancake cannot find any downgradable components
  * No components need to be downgraded
* Operation successfully completed
  * All components are downgraded
  * **And,** there is no Rhino 6 only component
* Some component\(s\) were downgraded successfully but some component\(s\) cannot be downgraded
  * Some component in the definition may be Rhino 6 only and has no substitution in Rhino 5
  * Some Sub/Mul component may have more than 2 inputs

### What else should I also notice?

* To-be-downgraded script shouldn't be opened in the document editor.
* The downgraded file is saved as `<OriginalFileName>_downgraded.gh` in the original location. So the original location must be writable.

