# Extended Context Menu

Pancake provides context-aware tools to help in several scenarios. The tools include component/parameter inspection, calculation profiling, wiring control, etc.

### How to use this feature?

* Select one or more components, **left-**click the canvas while holding Shift; or left-click any wire while holding Ctrl and Shift
* This feature is disabled in Safe mode.

### On a wire

![](../.gitbook/assets/image%20%283%29.png)

* Delete: Delete this wire.
* To source/target: Zoom to source/target
* Set as normal/faint/hidden: Set the style of the chosen wire to normal/faint/hidden
  * Notice: you will not be able to see the wire after it is changed "hidden". You need to right-click the target component to revert the setting.

### On a component/floating parameter

![](../.gitbook/assets/image%20%282%29.png)

* Set all input wires as normal/faint/hidden: Set the styles of all the input wires to normal/faint/hidden
* Inspect: Display a structured report of the component's information

### On a component parameter

![](../.gitbook/assets/image%20%284%29.png)

* Set all input wires as normal/faint/hidden: Set the styles of all the input wires to normal/faint/hidden
* Inspect component: Display a structured information report of the component the parameter belongs to
* Inspect parameter: Display a structured information report of the parameter, including **the order of inputs/outputs** from/to other components.

### On the canvas, after selecting one or more components

![](../.gitbook/assets/image%20%281%29.png)

* Profile selected components \(last run\): Display a processing time report of selected components. The information are collected from the last computation.
* Profile selected components \(new run\): Display a processing time report of selected components. Pancake will initiate new runs and measure processing time. Usually the result is more accurate but it takes more time to process, usually 10x-30x the time of a single run if your script is fast; 2x-5x the time of a single run if your script is time-consuming.
  * See [Performance Profiler](performance-profiler.md) for more information

