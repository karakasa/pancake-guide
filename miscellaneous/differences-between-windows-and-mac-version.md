# Differences between Windows and Mac version

Pancake \(short as PC\) is developed on Windows and targets Windows at the very beginning. Thanks to Mono, now one single Pancake binary supports both Windows and Mac platform. However, some features are unavailable on one platform. This page provides more information on the differences.

### File Block Monitor

The "allow apps downloaded from" feature of Mac doesn't affect Grasshopper plugins. Compared to Windows, macos doesn't have a similar mechanism that prevents GH from loading assemblies. So it's meaningless to provide the File Block Monitor.

### Hang Protection

PC uses [`Dispatcher.BeginInvoke`](https://docs.microsoft.com/en-us/dotnet/api/system.windows.threading.dispatcher.begininvoke?view=netframework-4.7.1#System_Windows_Threading_Dispatcher_BeginInvoke_System_Delegate_System_Object___) to run an empty probing procedure on the UI thread. If the invoke is completed in a period of time, PC takes the main thread as responsive. Otherwise, PC triggers an emergency save procedure, which will suspend the process, do the save, and resume the process. So a problem exists when main thread is busy, another computation thread is running and they are exchanging data. Under such situation, PC's suspending behavior will unsynchronize these two threads.

On Mac, the bug occurs that Mono runtime doesn't fully implement `Dispatcher` and cross-thread invoke is problematic. As a consequence, PC disables the feature on Mac.

### Portability Check

You cannot use "Copy To..." feature on macos. Due to a weird problem about `TableLayoutPanel` in Mono implementation, forms with automatic layout don't display correctly. Therefore, Portability Check uses a fallback presentation form on macos, which contains a textbox only.

