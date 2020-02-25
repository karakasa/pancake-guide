# Changelog

## 2.2.1.0 - 2020-02-20

### Added

* ImportFrom and ImportToDoc, that supports more general file import
* Example of general export, in line with the STL export example

### Changed

* Ribbon layout and menu, to reduce information overload
* Portability Report will include components exclusive to Rhino WIP
* Export components are better at dealing with inputs from Elefront, Human and InstanceManager
* Export3DM will copy layer styles if a layer with same name exists in the current Rhino document.

## 2.1.0.0 - 2019-12-25

### Added

* Support for geometric metadata
* Key-value-based associative array operations

## 2.0.0.0 - 2019-12-23

### Added

* **Pages in this manual will be ready soon. Read the new example files to see how new features work.**
* \[Param Access Overlay\] You may clearly see the access of a parameter, whether it is item, list or tree.
* \[Non-UI Export\] Non-UI Export is added for IGES, DAE, KMZ format. This feature requires Rhino 6 or higher version. These export don't rely on Rhino's user interface, therefore they are more reliable.
* \[Non-UI Export\] Text export is supported. You may use this feature to export any string, including Json.
* \[Quantity\] Added the capability to manipulate quantities, which are sets of amount and units. This is aimed for smoother engineering parametric practice.
* \[Associative Array\] Associative array is a set of values and optional name. It is treated as one single element when interacted with almost all other components. It may have a hierarchical structure. You may import/export data from/to various formats.
* \[Json\] Json read/write is now supported.
* \[Categorize\] You may now categorize data or count unique data easily.
* \[Default Value\] This component helps detecting null value as cluster input and replace it with default value.
* \[Definition Path\] This component yields the directory of current definition, so that you may reference external resources more easily.

## 1.9.1.0 - 2019-11-21

### Fixed

* "Export To STL" component will try to detect issues that prevent successful export
* Fixed a bug that may crash Mac Rhino

### Added

* Examples of several Export to STL usage are provided
* Capability to fully disable Extended Context Menu

## 1.8.1.0 - 2019-06-09

### Fixed

* Fixed a problem which may crash Rhino/Grasshopper on Mac

### Added

* Now you can assign keyboard shortcuts to many Pancake functions \(in Grasshopper Settings -&gt; Interface\).

## 1.8.0.0 - 2019-05-19

### Added

* \[Highlight manager\] Changes can be highlighted after an operation, such as [Internalizing Geometry](features/internalize-geometry.md), is done. You can switch the feature by "Settings"/"Highlight Changes".
* \[[Export to 3DM](components/export-to-3dm.md)\] Provides a reliable method to export geometries to an external 3DM file. This component doesn't rely on Rhino's user interface, therefore can be safely used in conjuction of any other procedure, compared to the [Export As](components/export-as.md) component.
* \[Portability Check\] The feature will also check for major [styling issues](features/portability-check.md#styling-check).

### Changed

* "Transfer settings" is moved inside "Setting" sub-menu.
* Code is cleaned to reduce the size of Pancake binary.
* Icons are changed and shown better in a low-DPI environment.

## 1.7.2.0 - 2018-12-26

### Fixed

* \[Extended menu\] Fixed the crash in Rhino 5. However, the feature of picking wire is currently unavailable due to lacking specific API from older versions of Grasshopper

## 1.7.1.0 - 2018-09-08

### Changed

* \[Extended menu\] Due to an unforseen conflict, the operation of Shift+LeftClick is changed to **Ctrl+**Shift+LeftClick.

## 1.7.0.0 - 2018-09-07

### Added

* [Extended context menu](features/extended-context-menu.md)
* [Setting transfer](features/setting-transfer.md)
* Undo histroy explorer
* Add-on explorer
* [Performance profiler](features/performance-profiler.md)

### Changed

* \[Downgrade to R5\] Online downgrading can be undone.
* \[Internalize Geometry\] The feature can be undone now.

### Fixed

* Simplified Chinese is fully supported. We also welcome you if you want to add another language to Pancake. Contact us for details.

## 1.6.2.0 - 2018-07-01

### Added

* Supported localization

### Changed

* \[Downgrade to R5\] Supported Relay component
* \[Portability Check\]  Better latest-version-only component recoginition in Mac GH

## 1.6.1.0 - 2018-06-13

### Added

* Mac support

## 1.6.0.0 - 2018-06-12

### Added

* \[Downgrade to R5\] ["Offline" downgrader](features/downgrade-components/downgrade-components-rhino-5.md). You can downgrade a file in Rhino 5
* [Filepath Series](components/filename-series.md)

### Changed

* \[Hang Protection\] Emergency saving is more reliable and no longer triggers "save failed" message boxes.

## 1.5.3.0 - 2018-06-02

### Added

* \[Export As\] Introduced a new compatible mode. It should solve some deadlock problems
* \[Export As\] New guidelines for export configuration \(see [here](components/export-as.md#important-notice-a-k-a-why-my-file-is-exported-with-wrong-options)\)

### Fixed

* \[Export As\] Solved that export isn't fully automated and stuck on the last step
* \[True-only Button\] Better interoperability with some components that may alter the solution status, such as `Export As`
* \[Cluster Op\] Name refreshing works normally now
* \[Cluster Op\] Merging inputs no longer blanks out downstream data

## 1.5.2.0 - 2018-05-30

### Fixed

* \[ClusterOp\] Fixed a bug that prevents Pancake merging inputs if there are 3 or more identical ones.

## 1.5.1.0 - 2018-05-24

### Fixed

* \[Core\] Implemented a hot fix that conducts a deeper check of validity of components and documents

## 1.5.0.0 - 2018-05-21

### Added

* [\[ClusterOp\] Merge identical cluster inputs](features/cluster-operations/merge-identical-inputs.md)
* [\[ClusterOp\] Refresh nicknames, names and descriptions of cluster parameters](features/cluster-operations/refresh-names.md)
* Developer mode
* DocObject info tool

## 1.4.1.0 - 2018-05-10

### Added

* Update notification. If a higher version of Pancake is available, you will see a green bar with "New version available..." in menu.

### Fixed

* \[True-only Button\] Fixed an error window pops up after you double clicked the button and move the mouse hovering the label part.

## 1.4.0.0 - 2018-05-07

### Added

* [Connectivity Analysis](features/connectivity-analysis.md)

### Changed

* \[Downgrade Components\] Failed components will be focused after the operation.
* \[Internalize Geometry\] Failed components will be focused after the operation.
* \[Version Watermark\] Menu items are rearranged.

## 1.3.1.0 - 2018-05-06

### Added

* \[Portability Check\] Now this feature reports core components unavailable in older version of GH

### Fixed

* \[Portability Check\] Fail to respond to the built-in version of GhPython shipped with Rhino 6

## 1.3.0.0 - 2018-05-05

### Added

* [Export As](components/export-as.md): directly export GH geometries to any format Rhino supports, with layer information \(if applicable\)
* \[Internalize Geometry\] Added a less destructive mode.

### Fixed

* \[True-only button\] Now the appearance is refreshed correctly. And the component no longer always evaluates `True` \(see [behavior](components/true-only-button.md#the-exact-behavior-of-true-only-button-as-of-1-3-0-0) section for more information\).
* \[Internalize Geometry\] Fixed a bug that prevents the feature from working.

### Changed

* \[Portability Check\] More plugins which cannot be easily copied are listed.
* \[Hang Protection\] Now the module gives more information on what happens.

## 1.2.0.0 - 2018-04-19

### Added

* [File block monitor](features/file-block-monitor.md): tell you when you need to unblock newly-installed plugins
* [Safe mode](miscellaneous/safe-mode.md)
* [True-only button](components/true-only-button.md)
* Wait Until component
* Distributed computing \(unavailable on Food4Rhino\): A framework that introduces multi-computer computation in Grasshopper environment. It can faciliate demanding jobs \(such as solar analysis\), by delegating tasks to different PCs.

### Fixed

* \[Hang Protection\] Now this feature correctly saves your document when the editor is inside a cluster. Before, the document wouldn't be saved.
* \[Hang Protection\] Now this feature correctly performs an emergency save to temporary folder if the original Grasshopper is never saved. Before, you would see a "sorry" message box.
* \[Hang Protection\] Now this feature is disabled, if Pancake is used on an unsupported platform \(such as Mac\).
* \[Downgrade to R5\] Now this feature checks if Subtraction and Multiplication are downgradable.
* \[Internalize Geometry\] Now this feature doesn't count already-internalized geometries towards success counter.

### Changed

* \[Hang Protection\] You no longer need to restart Rhinoceros to let the switch make effect.
* \[Hang Protection\] Sampling threshold is adjusted for better responsiveness.
* \[Portability Check\] Now this feature dives into a cluster and check all components used inside.
* \[Export to STL\] Now this component has a output, indicating if export is successful.

## 1.1.1.0 - 2018-03-20

### Added

* Export to STL component
* Rhino file version track



