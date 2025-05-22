# GeneralStatisticsSettingAtt (Object)

**_Interface for General statistic Controler._**

**Role** : the General statistics controler is a generic interface for all the thematics. One should never use it as a statistics thematic.

## Properties

### Property **Activation**( ) As boolean

Returns or sets the activation state of the statistics thematic.
**Role** : Returns or sets the value of statistics thematic activation.  
### Property **CPUS**( ) As boolean

Returns or sets the state ot the cpu time field.
**Role** : Returns or sets the state ot the cpu time field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **CumulationMode**( ) As boolean

Returns or sets the cumulation state of the statistics thematic.
**Role** : Returns or sets the value of statistics thematic cumulation.  
### Property **DateFormat**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the state ot the date format field.
**Role** : Returns or sets the state ot the date format field.

**Parameters:**

` iDateFormat`      **Legal values** :
`StandardDate :` default date format (Mon Jan 1 08:00.00 2000)
`NumericalDate:` numerical date format(2000.001.08.00.00)
`NumericalDateMilliecond:` numerical date format(2000.001.08.00.00.000)

### Property **ELPS**( ) As boolean

Returns or sets the state ot the elapsed time field.
**Role** : Returns or sets the state ot the elapsed time field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **HOST**( ) As boolean

Returns or sets the state ot the host name field.
**Role** : Returns or sets the state ot the host name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **Output**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the output format of the statistics thematic.
**Role** : Returns or sets the output format of the statistics thematic.

**Parameters:**

` oOutputType`      **Legal values** :
`File :` statistics are outputed in a file
`Console:` statistics are outputed on the console (if available)

### Property **OutputFile**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the path of the statistics thematic file.
**Role** : Returns or sets the path of the statistics thematic file.  
### Property **OutputFormat**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the state ot the output format field.
**Role** : Returns or sets the state ot the output format field.

**Parameters:**

` iOutputFormat`      **Legal values** :
`StandardOutput:` default format
`NoThematics :` the thematic name is not repeated on each line

### Property **RTIM**( ) As boolean

Returns or sets the state ot the response time field.
**Role** : Returns or sets the state ot the response time field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **THEM**( ) As boolean

Returns or sets the state ot the thematic field.
**Role** : Returns or sets the state ot the thematic field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **TIME**( ) As boolean

Returns or sets the state ot the time and date field.
**Role** : Returns or sets the state ot the time and date field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **TimeUnit**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the state ot the time unit field.
**Role** : Returns or sets the state ot the time unit field.

**Parameters:**

` iTimeUnit`      **Legal values** :
`Second :` durations are in seconds
`Millisecond:` durations are in milliseconds

### Property **UPID**( ) As boolean

Returns or sets the state ot the user pid field.
**Role** : Returns or sets the state ot the user pid field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated

### Property **USER**( ) As boolean

Returns or sets the state ot the user name field.
**Role** : Returns or sets the state ot the user name field.

**Parameters:**

` oStatus`      **Legal values** :
`TRUE :` the field is activated
`FALSE:` the field is not activated
Methods

### Func **GetFormatMode**( long  `flag`) As boolean

Returns the format mode of the statistics thematic.
**Role** : Returns or sets the format mode of the statistics thematic.

**Parameters:**

` oFormatMode`      **Legal values** :
`TRUE :` the thematic output is formated (field="value").
`FALSE:` the thematic output is not formated ("value").

### Func **GetThematicsParameterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves environment informations for the general statistics parameters.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetFormatMode**( boolean  `iFormatMode`,  long  `flag`)

Sets the format mode of the statistics thematic.
**Role** : Returns or sets the format mode of the statistics thematic.

**Parameters:**

` iFormatMode`      **Legal values** :
`TRUE :` the thematic output is formated (field="value").
`FALSE:` the thematic output is not formated ("value").

### Sub **SetThematicsParameterLock**( boolean  `iLocked`)

Locks or unlocks the general statistics parameters.
**Role** :Locks or unlocks the statistics parameters.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure