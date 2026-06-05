# miscellaneous
Miscellaneous (things, junk): refers to a varied collection of unrelated, often low-value items that don't fit into a specific category.


### Identify Which Process Is Blocking a File in Windows Using Process Explorer

Process Explorer is a _free_ tool from **Microsoft Sysinternals**:

You can acquire Process Explorer using the following WingGet command from command line prompt:

```
Winget install Microsoft.Sysinternals.ProcessExplorer
```

```
In Process Explorer, Go to **Find > Find Handle or DLL**.
```

```
Type part of the file or folder name and click Search.
```

The tool will list all processes currently using the file. Click an entry to highlight the process in the main window.
You can _right-click_ the handle and select **Close Handle** to release the file (use with caution).
