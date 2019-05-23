# Performance Profiler

{% hint style="info" %}
This article is not completed yet. Now it only provides basic information.
{% endhint %}

For Grasshopper script designers, it is important to know what components take longer time and where is the bottleneck. Pancake provides a tool of profiling a part of your script with higher accuracy and error control.

### How to use this feature?

* Select one or more components,
* Left-click an empty place on the canvas while holding Ctrl and Shift
* Click **Profile selected components \(new run\)**
* Wait for a while. The process can take at least 5 seconds and up to 10 times the duration of a single run.

### How to interpret the report?

A typical report reads like \(some lines are omitted\):

```text
Performance report of 124 object(s):
PancakeDev is required for detailed timing and monitoring.

Computation time of the selected:
    00:00:00.4712146
Computation time of the document:
    00:00:00.4712146
Proportion:
    100.00%

Repeated:
    11 times

Bottleneck (individual):
    98.89% 0:00:00:00.4660076 (-34.84% ~ +30.47%) Brep | Plane
    00.55% 0:00:00:00.0025779 (-14.38% ~ +45.33%) Trimzero
    00.07% 0:00:00:00.0003161 (-05.21% ~ +14.79%) StripMeshToBRep
    00.06% 0:00:00:00.0002953 (-11.48% ~ +48.67%) Curvature
    00.04% 0:00:00:00.0001777 (-11.86% ~ +49.49%) Angle
    00.03% 0:00:00:00.0001258 (-14.02% ~ +57.81%) Pick'n'Choose
    00.02% 0:00:00:00.0000983 (-42.71% ~ +51.53%) Shatter
    00.02% 0:00:00:00.0000918 (-09.00% ~ +29.26%) Orient
    ....

Bottleneck (grouped):
    98.89% 0:00:00:00.4660076 Brep | Plane
    00.63% 0:00:00:00.0029633 Trimzero
    00.06% 0:00:00:00.0002953 Curvature
    00.04% 0:00:00:00.0001882 Pick'n'Choose
    00.04% 0:00:00:00.0001777 Angle
    00.02% 0:00:00:00.0000983 Shatter
    00.02% 0:00:00:00.0000918 Orient
    00.01% 0:00:00:00.0000700 Perp Frames
    ....

```



