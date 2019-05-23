# Export to 3DM

This component exports Grasshopper geometries to an external 3DM Rhino file. This feature doesn't rely on user interface, therefore it is more reliable and can be safely conducted anytime.

### How to use this component?

* The component is listed under Pancake tab, I/O
* Or you can find it via double-clicking

### What does each parameter mean?

{% tabs %}
{% tab title="Input" %}
| ickname | Description |
| :--- | :--- |
| Geo | The geometr\(ies\) you want to export |
| Layer | Layer path\(s\) to save the corresponding geometr\(ies\). Can be empty. See [here](export-as.md#how-to-define-layers-for-each-geometry) for help. |
| ObjAttr | Object attributes. See below. Can be empty. |
| File | Where to save the file |
| Overwrite | Control if the destination should be overwritten. `False` by default. |
| Ver | Can be `0`, or from `2` to current version. `0` means the latest version. `0` by default. |
| Export | Feed true to export the geometries. |
{% endtab %}

{% tab title="Output" %}
| Nickname | Description |
| :--- | :--- |
| OK | Evaluates true when the export is successful |
| Log | Operation log when error occurs |
{% endtab %}
{% endtabs %}

### What geometries are supported?

* Arc
* Box
* BRep
* Circle
* Curve
* Ellipse
* Hatch
* Line
* Mesh
* Point3d
* Surface
* TextDot

Annotations are generally unsupported.

### What else should I also notice?

* Under Rhino 5, level designation is ignored due to API limitation. All geometries are put onto the default layer.
* Layer information in object attributes is ignored.
* Object attributes from Elefront is unsupported. We recommend to generate it through Human.
* We don't recommend you to use any object attribute other than colour, because they are not tested.

