# ManufacturingActivity (Object)

**_ManufacturingActivity defines a set of methods and mainly adds some specific methods and services in Manufacturing on ProcessPlan Activities._**
Some methods have to be used carefully, they can have no meanly on a specific Activity. This methods allows to support operation from other domain either then Manufacturing.

## Properties

### Property **Active**( ) As boolean

Returns the activation state of the activity.

**Returns:**      oActive The activation state of the activity  **Example:**     The following example returns in `bActive` the activation state of the activity `firstActivity`:

```VBScript
Dim firstActivity As ManufacturingActivity
Set firstActivity = ...
Dim bActive As boolean
Set bActive = firstActivity.Active

```

### Property **MachinableFeature**( ) As [CATIAManufacturingMachinableArea](../ManufacturingInterfaces/interface_ManufacturingMachinableArea_149911.md)

Retrieve the machinable area of a Manufacturing Activity.

**Example:**     The following example retrieves in `theMAF` the machinable area of the activity `firstActivity`.

```VBScript
Dim firstActivity As ManufacturingActivity
Set firstActivity = ...
Dim theMAF As ManufacturingMachinableArea
Set theMAF = firstActivity.MachinableArea

```

### Property **MachiningTime**( ) As double (Read Only)

Retreive the milling time of a Manufacturing Activity.

**Example:**     The following example retreives in `theMachiningTime` the time when the tool meets the workpiece (in minutes).

```VBScript
theMachiningTime = firstActivity.MachiningTime

```

### Property **NumberOfFeedrateAttributes**( ) As short (Read Only)

This property returns the number of Feedrate attributes of a Manufacturing Activity.  
### Property **NumberOfGeomAttributes**( ) As short (Read Only)

This property returns the number of Geometry attributes of a Manufacturing Activity.  
### Property **NumberOfStrategyAttributes**( ) As short (Read Only)

This property returns the number of Strategy attributes of a Manufacturing Activity.  
### Property **Precedences**( ) As [CATIAManufacturingPrecedences](../ManufacturingInterfaces/interface_ManufacturingPrecedences_122094.md) (Read Only)

This property returns the interface which manages the precedences on the operation. These collection defines the list of precedences for a manufacturing Activity.

**Example:**     The following example returns in `precedences` the interface that manage the precedences for the `myActivity` Activity :

```VBScript
...
Set myActivity  = ...
Set precedences = myActivity.Precedences

```

### Property **Representation**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

This property returns the path of the representation file for a manufacturing Activity.  
### Property **Tool**( ) As [CATIAManufacturingTool](../ManufacturingInterfaces/interface_ManufacturingTool_62710.md) (Read Only)

Retreive the Tool of a Manufacturing Activity.

**Example:**     The following example retreives in `CurTool` the manufacturing tool of Manufacturing Activity `firstActivity`

```VBScript
Set CurTool = firstActivity.GetTool

```

### Property **ToolAssembly**( ) As [CATIAManufacturingToolAssembly](../ManufacturingInterfaces/interface_ManufacturingToolAssembly_133824.md) (Read Only)

Retreive the ToolAssembly of a Manufacturing Activity.

**Example:**     The following example retrieves in `CurrAssembly` the manufacturing tool assembly of the manufacturing activity `CurrActivity`

```VBScript
Set CurrAssembly = CurrActivity.ToolAssembly

```

### Property **TotalTime**( ) As double (Read Only)

Retreive the total Time of a Manufacturing Activity.

**Example:**     The following example retreives in `theTotalTime` the total time of the activity firstActivity (in minutes).

```VBScript
theTotalTime = firstActivity.TotalTime

```

### Property **VideoResult**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Retreive the video result path of a Manufacturing Activity. The path is empty if no video result.

**Example:**     The following example retreives in `theVideoResult` the video result of the activity firstActivity (in minutes).

```VBScript
theVideoResult = firstActivity.VideoResult

```

Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retreive the Attribute of a Manufacturing Activity.

**Example:**     The following example retreives in `RapidFeed` the attribute `MfgRapidFeed` of Manufacturing Activity `firstActivity`

```VBScript
Set RapidFeed = firstActivity.GetAttribute(MfgRapidFeed)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieve the NLS name from the attribute name of a Manufacturing Activity.

### Sub **GetListOfFeedrateAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Feedrate attributes of a Manufacturing Activity.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of feedrate attributes of the Manufacturing Activity `myActivity`

```VBScript
call myActivity.GetListOfFeedrateAttributes(oListOfAttributes)

```

### Sub **GetListOfGeomAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Geometry attributes of a Manufacturing Activity.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Geometry attributes of the Manufacturing Activity `myActivity`

```VBScript
call myActivity.GetListOfGeomAttributes(oListOfAttributes)

```

### Sub **GetListOfStrategyAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Strategy attributes of a Manufacturing Activity.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Strategy attributes of the Manufacturing Activity `myActivity`

```VBScript
call myActivity.GetListOfStrategyAttributes(oListOfAttributes)

```

### Sub **GetMachiningDirection**( double  `oXAxis`,  double  `oYAxis`,  double  `oZAxis`)

Retreives the Machining Direction coordinates of a Manufacturing Operation.

### Sub **GetToolAxis**( double  `oXAxis`,  double  `oYAxis`,  double  `oZAxis`)

Retreives the ToolAxis coordinates of a Manufacturing Activity.

### Sub **SetMachiningDirection**( double  `iXAxis`,  double  `iYAxis`,  double  `iZAxis`)

Defines the Machining Direction coordinates of a Manufacturing Operation.

### Sub **SetToolAxis**( double  `iXAxis`,  double  `iYAxis`,  double  `iZAxis`)

Defines the ToolAxis coordinates of a Manufacturing Activity.