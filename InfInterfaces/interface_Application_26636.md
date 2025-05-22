# Application (Object)

**_Represents the current CNext application and its frame window._**
The application is the root object for all the other objects you can use and access from scripts. It directly aggregates:

  * The document collection represented by the [Documents](../InfInterfaces/interface_Documents_18392.md) object. This collection contains all the documents currently opened by the application
  * The window collection represented by the [Windows](../InfInterfaces/interface_Windows_11431.md) object. This collection contains all the windows currently opened by the application, each window displaying one of the documents contained in the document collection
  * The [SystemService](../System/interface_SystemService_36846.md) object, providing information about the system environment.

The active document and the active window are two key objects for the application you can access using the ActiveDocument and ActiveWindow properties respectively. The active window is the window the end user is currently working in, and the active document is the document displayed in this active window and that the end user is being editing. This document sets its workshop, that is the available menus and toolbars that make it possible to edit it, according to its type.

When you create or use macros for in-process access, the application is always referred to as `CATIA`.

## Properties

### Property **ActiveDocument**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md) (Read Only)

Returns the active document. The active document is the document the end user is being editing.

**Example:**      This example retrieves in `ActiveDoc` the active document of the `CATIA` application.

```VBScript
Dim ActiveDoc As Document
Set ActiveDoc = CATIA.ActiveDocument

```

### Property **ActivePrinter**( ) As [CATIAPrinter](../InfInterfaces/interface_Printer_11274.md)

Returns or sets the active printer. The active printer is the printer on which documents are printed

**Example:**      This example retrieves in `ActivePrinter` the active printer of the `CATIA` application.

```VBScript
Dim ActivePrinter As Printer
Set ActivePrinter = CATIA.ActivePrinter

```

### Property **ActiveWindow**( ) As [CATIAWindow](../InfInterfaces/interface_Window_8384.md) (Read Only)

Returns the active window. The active window is the window in which the end user is currently editing the active document.

**Example:**      This example retrieves in `ActiveWin` the active window of the `CATIA` application.

```VBScript
Dim ActiveWin As Window
Set ActiveWin = CATIA.ActiveWindow

```

### Property **CacheSize**( ) As long

Returns or sets the default local cache size used by the application.

**Example:**      This example sets the cache size for by the `CATIA` application to those defined in `LocalCacheSize`.

```VBScript
LocalCacheSize= 10
CATIA.CacheSize = LocalCacheSize

```

### Property **Caption**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the application's window title. This title is displayed in the application's window title bar.

**Example:**      This example retrieves in `Title` the `CATIA` application's window title.

```VBScript
Title = CATIA.Caption

```

The returned value is like this:

```VBScript
CNext

```

### Property **DisplayFileAlerts**( ) As boolean

Returns or sets the application ability to display file alerts.
**True** if the application enables file alert display.
True is the default. A file alert is, for example, the dialog box that prompts you that the file you want to save is in read only mode, or that the file you want to close needs to be saved. It could be handy to disable these file alerts for automation since they may freeze your macro execution, waiting for an end user input in the displayed dialog box.

**Example:**      This example disables file alerts for the `CATIA` application.

```VBScript
CATIA.DisplayFileAlerts = False

```

### Property **Documents**( ) As [CATIADocuments](../InfInterfaces/interface_Documents_18392.md) (Read Only)

Returns the collection of documents currently managed by the application.

**Example:**      This example retrieves in `DocCollection` the collection of documents currently managed by the `CATIA` application.

```VBScript
Dim DocCollection As Documents
Set DocCollection = CATIA.Documents

```

### Property **FileSearchOrder**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the default path concatenation used by the application to search for when opening files.

**Example:**      This example sets the paths to search for by the `CATIA` application to those defined in `PathConcatenation`.

```VBScript
PathConcatenation = "/u/users/fbq/db/model:/u/users/psr/db/model"
CATIA.FileSearchOrder = PathConcatenation

```

Theese methods require the installation of CATIA - PPR xPDM Gateway 1 Product (PX1) In case this product is not granted, the first invocation to one of the methods will fail.  
### Property **FileSystem**( ) As [CATIAFileSystem](../InfInterfaces/interface_FileSystem_22052.md) (Read Only)

Returns the file system. The file system provides access to a computer's file system.

**Example:**      This example retrieves in `AppliFileSys` the file sytem of the `CATIA` application.

```VBScript
Dim AppliFileSys As FileSystem
Set AppliFileSys = CATIA.FileSystem

```

### Property **FullName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the application's executable file full name, including its path. This name is the name of the executable file used to start the application.

**Example:**      This example retrieves in `ApplicationFullName` the `CATIA` application's executable file full name.

```VBScript
ApplicationFullName = CATIA.FullName

```

The returned value is like this:

```VBScript
\\lisa\cxr1arel\bsf\alpha_a\code\bin\CNEXT.exe

```

### Property **HSOSynchronized**( ) As boolean

Returns or sets the HSO synchronization compared with the CSO.
**Role** : Precises if, for all [Selection](../InfInterfaces/interface_Selection_18040.md) object instances, the HSO (Highlighted Set of Objects) is synchronized compared to the CSO (Current Set of Objects). Valid values are:

  * **True** : Whatever the [Selection](../InfInterfaces/interface_Selection_18040.md) object instance, the [Selection](../InfInterfaces/interface_Selection_18040.md) object methods which write into the CSO update also the HSO.
At the beginning of a script execution, the property is set to True. This implies that regarding a script which:
    * does not modify this property
    * asks the end user to select the edge of a Pad
    * creates then a fillet taking the edge as specification
    * asks then the end user to select a face of the Pad to create a hole
during the script execution, when the end user will be asked to select a face, if he/she selects Edit\Undo, he/she will see:
    * The fillet highlighted in the [Document](../InfInterfaces/interface_Document_14456.md) window
    * The fillet deleted
The fillet will have blinked.
  * **False** : opposite behavior. This prevents the features from blinking between two user interactions when scripting an interactive command.

**Note** : even if this property is set to False, at the begining of one of the following methods:

  * Selection.SelectElement2
  * Selection.SelectElement3
  * Selection.SelectElement4
  * Selection.IndicateOrSelectElement2D
  * Selection.IndicateOrSelectElement3D
  * Application.StartCommand

for all [Document](../InfInterfaces/interface_Document_14456.md) objects, the HSO is synchronized in comparison to the CSO. **CAUTION** : the use of the False value for this property requires the following scripting rules, so that, when the user is asked to select a feature in the active window, the HSO be up to date. If these rules were not respected, this would lead to unpredictable results:

  * VBScript case:

```VBScript
    CATIA.HSOSynchronized=False                  'the property will be set to False at the
                                                 'beginning of the script
    . . .
    CATIA.HSOSynchronized=True                   'the property must be set to True before
    MsgBox "The result is correct"               'each call to the MsgBox or InputBox
    CATIA. HSOSynchronized=False                 'functions, and set to False after
    . . .
    Status=Selection.SelectElement2(InputObjectType, _
                                    "Select a 1-D entity whose geometry is rectilinear",false)
    if (Status = "Cancel") then
   '  we go out
        CATIA.HSOSynchronized=True               'the property must be set to True before
        Exit Sub                                 'going out of the script
    else
     . . .
    CATIA.HSOSynchronized=True                   'the property must be set to True before
    End Sub                                      'the end of the script
```

  * Visual Basic for Applications or Visual Basic 6 Development Studio case:

```VBScript
    Sub CATMain()
    CATIA.HSOSynchronized=False                  'the property will be set to False at the
                                                 'beginning of the CATMain procedure
     . . .
    Status=Selection.SelectElement2(InputObjectType, _
                                    "Select a 1-D entity whose geometry is rectilinear",false)
    if (Status = "Cancel") then
   '  we go out
        CATIA.HSOSynchronized=True               'the property must be set to True before
        Exit Sub                                 'going out of the script
    else
     . . .
    CATIA.HSOSynchronized=True                   'the property must be set to True before
    End Sub                                      'the end of the CATMain procedure

    Private Sub CommandButton_Click()
    CATIA.HSOSynchronized=False                  'the property must be set to False at
                                                 'the beginning of any form or object class
                                                 'method
     . . .
    CATIA.HSOSynchronized=True                   'the property must be set to True before
    End Sub                                      'the end of the method

```

**CAUTION** : the False value for this parameter should not be set for a script which automates a task: when the CSO and the HSO are not synchronized, performance is impacted. 
### Property **Height**( ) As float

Returns or sets the height of the application's frame window. The height is expressed in pixels.

**Example:**      This example sets the height of the `CATIA` application's frame window to 300 pixels.

```VBScript
CATIA.Height = 300

```

### Property **Interactive**( ) As boolean

Returns or sets the application sensitivity to end user interactions.
**True** if the application is end user interaction sensitive.

**Example:**      This example makes the `CATIA` application sensitive to end user interactions.

```VBScript
CATIA.Interactive = True

```

### Property **Left**( ) As float

Returns or sets the distance from the application's frame window left side to the left side of the screen. This distance is expressed in pixels.

**Example:**      This example sets the distance from the `CATIA` application's frame window left side to the left side of the screen to 150 pixels.

```VBScript
CATIA.Left = 150

```

### Property **LocalCache**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the default local cache path used by the application.

**Example:**      This example sets the cache path for by the `CATIA` application to those defined in `LocalCachePath`.

```VBScript
LocalCachePath= "/tmp/cache"
CATIA.LocalCache = LocalCachePath

```

### Property **Path**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the path of the application's executable files.

**Example:**      This example retrieves in `ApplicationPath` the path where the `CATIA` application executable files are located.

```VBScript
ApplicationPath = CATIA.Path

```

The returned value is like this:

```VBScript
\\lisa\cxr1arel\bsf\alpha_a\code\bin

```

### Property **Printers**( ) As [CATIAPrinters](../InfInterfaces/interface_Printers_14774.md) (Read Only)

Returns the collection of the printers currently managed by the application.

**Example:**      This example retrieves in `PrintersCollection` the collection of the printers currently managed by the `CATIA` application.

```VBScript
Dim PrintersCollection As Windows
Set PrintersCollection = CATIA.Printers

```

### Property **RefreshDisplay**( ) As boolean

Enables or disables the update of the display during the script replay. To improve performance, this update can be temporarely disabled by setting this property to False in the script.
**True** if the application's display is refreshed after each method call (value set by default).

**Example:**      This example makes the update of the `CATIA` application's display disabled during the script replay.

```VBScript
CATIA.RefreshDisplay = False

```

### Property **StatusBar**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the text displayed in the application's window status bar.

**Example:**      This example retrieves in `Text` the text displayed in the `CATIA` application's window status bar.

```VBScript
Text = CATIA.StatusBar

```

The returned value is like this:

```VBScript
Welcome to CATIA CxR1

```

### Property **SystemConfiguration**( ) As [CATIASystemConfiguration](../InfInterfaces/interface_SystemConfiguration_78951.md) (Read Only)

Returns the system configuration object (an object which provides access to system or configuration dependent resources).

**Parameters:**

` oConfiguration`      The system configuration object.

### Property **SystemService**( ) As [CATIASystemService](../System/interface_SystemService_36846.md) (Read Only)

Returns system services.

**Example:**      This example retrieves in `AppliSysSer` the `CATIA` application's system services.

```VBScript
Dim AppliSysSer As SystemService
Set AppliSysSer = CATIA.SystemService

```

### Property **Top**( ) As float

Returns or sets the distance from the application'si frame window top to the top of the screen. This distance is expressed in pixels.

**Example:**      This example sets the distance from the `CATIA` application's frame window top to the top of the screen to 50 pixels.

```VBScript
CATIA.Top = 50

```

### Property **Visible**( ) As boolean

Returns or sets the application's window visibility.
**True** if the application's window is visible to the end user.

**Example:**      This example makes the `CATIA` application's window visible.

```VBScript
CATIA.Visibility = True

```

### Property **Width**( ) As float

Returns or sets the width of the application's frame window. The width is expressed in pixels.

**Example:**      This example sets the width of the `CATIA` application's frame window to 350 pixels.

```VBScript
CATIA.Width = 350

```

### Property **Windows**( ) As [CATIAWindows](../InfInterfaces/interface_Windows_11431.md) (Read Only)

Returns the collection of windows currently managed by the application.

**Example:**      This example retrieves in `WinCollection` the collection of windows currently managed by the `CATIA` application.

```VBScript
Dim WinCollection As Windows
Set WinCollection = CATIA.Windows

```

Methods

### Func **CreateSendTo**( ) As [CATIASendToService](../InfInterfaces/interface_SendToService_35734.md)

Creates a Send TO.
**Role:** This method creates a [SendToService](../InfInterfaces/interface_SendToService_35734.md) instance.
Warning : CATIASendToService interface requires the installation of CATIA - PPR xPDM Gateway 1 Product (PX1) In case this product is not granted, the first invocation to one of CATIASendToService methods will fail.  
### Func **FileSelectionBox**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTitle`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtension`,  [CatFileSelectionMode](../InfInterfaces/enum_CatFileSelectionMode_82442.md)  `iMode`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Displays a modal dialog box which can be used to select / enter the name of a file to open / save.

**Parameters:**

` iTitle`      The title of the dialog box.
` iExtension`      A file extension filter.
` iMode`      The mode in which to run the dialog box (either `CatFileSelectionModeOpen` or `CatFileSelectionModeSave`.
` oFilePath`      The return string containing the full path of the selected file, or a zero-length string if the user selects `Cancel`.

**Example:**      This example asks the user to select a text file and prints the path of the selected file.

```VBScript
filepath = CATIA.FileSelectionBox("Select a text file", "*.txt", CatFileSelectionModeOpen)
CATIA.SystemServices.Print "The selected file is " & filepath

```

### Func **GetWorkbenchId**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the identifier of the CATIA current workbench.

**Parameters:**

` oworkbenchId`      The id of the current workbench.

### Sub **Help**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iHelpID`)

Displays application's online help.

**Parameters:**

` iHelpID`      Identifier of the help message to display  **Example:**      This example displays the string referred to by the `HelpKey` message key in the message catalog concatenation.

```VBScript
CATIA.Help("HelpKey")

```

### Sub **Quit**( )

Exits the application and closes all open documents.

**Example:**      This example exits the `CATIA` application and closes all its open documents.

```VBScript
CATIA.Quit()

```

### Sub **StartCommand**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCommandId`)

Starts a CATIA command.
**Role:** This method starts a command and executes it untill its first interaction. Please notice interactions such as selections you could add after in your macro will not work. StartCommand is useful to execute one-shot (not interactive) commands, it is not safe for interactive commands.

**Parameters:**

` iCommandId`      The id of the command to be started. This id can be the name of the command or its alias.

### Sub **StartWorkbench**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iworkbenchId`)

Starts a CATIA workbench.

**Parameters:**

` iworkbenchId`      The id of the workbench to be started.