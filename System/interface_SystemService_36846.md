# SystemService (Object)

**_Represents an object which provides system services._**

## Methods

### Func **Environ**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iEnvString`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the value of an environment variable.

**Parameters:**

` iEnvString`      The name of the environment variable  **Example:**      This example retrieves the value of the `PATH` variable in the `Value` string.

```VBScript
     Value = CATIA.SystemService.Environ("PATH")

```

### Func **Evaluate**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iScriptText`,  [CATScriptLanguage](../System/enum_CATScriptLanguage_59191.md)  `iLanguage`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFunctionName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iParameters`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Evaluates a scripted function.

**Parameters:**

` iScriptText`      The program text
` iLanguage`      The language the program is written in
` iFunctionName`      The name of the function to invoke
` iParameters`      An array of parameters for the function
` oResult`      The value returned by the function (if any)  **Example:**      This example executes the function CATMain in the program Macro1.catvbs contained by Part1.CATPart

```VBScript
     Dim params()
     CATIA.SystemService.Evaluate"Sub CATMain\nMsgBox \"Hello, World\"\nEnd Sub", CATVBScriptLanguage, "CATMain", params

```

### Func **ExecuteBackgroundProcessus**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExecutablePath`) As long

   Executes an asynchronous process. This process is launched in background and `ExecuteBackgroundProcess` doesn't wait for it to complete. If the executable to run needs a specific environment to works correctly (for example environment variables like PATH or LD_LIBRARY_PATH correctly set), this environment must have been set in order to make this method succeed. If this executable needs to be launched from a window, this method will fail.

**Parameters:**

` iExecutablePath`      The path of the executable to run and its arguments If the executable is not present in the PATH environment variable, you must specify its complete absolute path. If this path contains blanks, you must enclose it with the simple quote character ''' : for example CATIA.SystemService.ExecuteBackgroundProcess "'C:\Program Files\myApp\myApp.exe' myArg".

**Returns:**      Non significative return code. It's never the asynchronous process return code  **Example:**      This example executes the command located at
```

```VBScript
and doesn't wait the end of its execution.

```VBScript
     CATIA.SystemService.ExecuteBackgroundProcessus ""

```

### Func **ExecuteProcessus**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExecutablePath`) As long

   Executes a synchronous process. If this process is succesfully launched, `ExecuteProcessus` waits for it to terminate and returns the process return code. If the executable to run needs a specific environment to works correctly (for example environment variables like PATH or LD_LIBRARY_PATH correctly set), this environment must have been set in order to make this method succeed. If this executable needs to be launched from a window, this method will fail.

**Parameters:**

` iExecutablePath`      The path of the executable to run and its arguments. If the executable is not present in the PATH environment variable, you must specify its complete absolute path. If this path contains blanks, you must enclose it with the simple quote character ''' : for example CATIA.SystemService.ExecuteProcessus "'C:\Program Files\myApp\myApp.exe' myArg".

**Returns:**      The synchronous process return code  **Example:**      This example executes the command located at
```

```VBScript
waits for it to end, and returns its return code.

```VBScript
     ReturnCode = CATIA.SystemService.ExecuteProcessus("")

```

### Func **ExecuteScript**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLibraryName`,  [CatScriptLibraryType](../System/enum_CatScriptLibraryType_85292.md)  `iType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProgramName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFunctionName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iParameters`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Executes a scripted function.

**Parameters:**

` iLibraryName`      The library in which the script is contained
` iLibraryType`      The type of the library
` iProgramName`      The name of the program in the library
` iFunctionName`      The name of the function to invoke
` iParameters`      An array of parameters for the function
` oResult`      The value returned by the function (if any)  **Example:**      This example executes the function CATMain in the program Macro1.catvbs contained by Part1.CATPart

```VBScript
     Dim params()
     CATIA.SystemService.ExecuteScript"Part1.CATPart", catScriptLibraryTypeDocument, "Macro1.catvbs", "CATMain", params

```

### Sub **Print**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iString`)

   Prints a string on stdout.

**Parameters:**

` iString`      The string to print  **Example:**      This example prints the string "Hello world!".

```VBScript
     CATIA.SystemService.Print("Hello world!")

```