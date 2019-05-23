# Internalize Geometry

Pancake can help you internalize all referenced geometries in one click. This can be useful when you want to exchange your Grasshopper script without the Rhino file. As of 1.3.0.0, a [less destructive mode](internalize-geometry.md#what-is-less-destructive-mode) is introduced.

### How to use this feature?

* Navigate to "Pancake" menu, click "Internalize referenced geometry"

### What types of geometry will be internalized?

* Arc
* Box
* BRep
* Circle
* Curve
* Line
* Rectangle
* Mesh
* Plane
* Surface
* Twisted box
* Plankton mesh
* Elefront geometries

This list might be incomplete. Pancake cannot guarantee support for third-party geometry. Please contact us if you think this feature isn't working as intended. Technically, only those that implement `IGH_GeometricGoo` and `IGH_PersistentParam` interfaces are included.

### What is "less destructive mode"?

* In former versions, internalization will trigger script-wide recomputation, which is sometimes time-consuming and laggy.
* In the less destructive mode, recomputation will be suppressed. Pancake manipulates the data without informing Grasshopper framework.
* However, due to the cache nature of Grasshopper, the tooltips of internalized geometries stay as "Referenced XXX". Therefore, you need to save your script or trigger recomputation manually to make the text change.
* The mode could be switched on by holding Shift key when clicking the menu item.



