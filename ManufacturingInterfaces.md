# ManufacturingInterfaces Framework

## Object Index

  * [MachiningProcess](ManufacturingInterfaces/interface_MachiningProcess_55046.md)
  * [ManufacturingAPTGenerator](ManufacturingInterfaces/interface_ManufacturingAPTGenerator_129376.md)
  * [ManufacturingActivity](ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)
  * [ManufacturingCopyTransformation](ManufacturingInterfaces/interface_ManufacturingCopyTransformation_207460.md)
  * [ManufacturingFeature](ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)
  * [ManufacturingFeatures](ManufacturingInterfaces/interface_ManufacturingFeatures_95125.md)
  * [ManufacturingGeneratorData](ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)
  * [ManufacturingHole](ManufacturingInterfaces/interface_ManufacturingHole_61666.md)
  * [ManufacturingInsert](ManufacturingInterfaces/interface_ManufacturingInsert_78415.md)
  * [ManufacturingMachinableArea](ManufacturingInterfaces/interface_ManufacturingMachinableArea_149911.md)
  * [ManufacturingMachinableFeature](ManufacturingInterfaces/interface_ManufacturingMachinableFeature_187924.md)
  * [ManufacturingMachinableGeometry](ManufacturingInterfaces/interface_ManufacturingMachinableGeometry_202868.md)
  * [ManufacturingMachine](ManufacturingInterfaces/interface_ManufacturingMachine_84488.md)
  * [ManufacturingMachiningAxis](ManufacturingInterfaces/interface_ManufacturingMachiningAxis_142294.md)
  * [ManufacturingOperation](ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)
  * [ManufacturingOutput](ManufacturingInterfaces/interface_ManufacturingOutput_79839.md)
  * [ManufacturingOutputGenerator](ManufacturingInterfaces/interface_ManufacturingOutputGenerator_169508.md)
  * [ManufacturingPattern](ManufacturingInterfaces/interface_ManufacturingPattern_86712.md)
  * [ManufacturingPrecedence](ManufacturingInterfaces/interface_ManufacturingPrecedence_111444.md)
  * [ManufacturingPrecedences](ManufacturingInterfaces/interface_ManufacturingPrecedences_122094.md)
  * [ManufacturingProcess](ManufacturingInterfaces/interface_ManufacturingProcess_86742.md)
  * [ManufacturingProgram](ManufacturingInterfaces/interface_ManufacturingProgram_86282.md)
  * [ManufacturingSetup](ManufacturingInterfaces/interface_ManufacturingSetup_70728.md)
  * [ManufacturingTool](ManufacturingInterfaces/interface_ManufacturingTool_62710.md)
  * [ManufacturingToolAssembly](ManufacturingInterfaces/interface_ManufacturingToolAssembly_133824.md)
  * [ManufacturingToolCorrector](ManufacturingInterfaces/interface_ManufacturingToolCorrector_145356.md)
  * [ManufacturingToolMotion](ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)
  * [ManufacturingView](ManufacturingInterfaces/interface_ManufacturingView_62589.md)
  * [MfgActivities](ManufacturingInterfaces/interface_MfgActivities_36625.md)
  * [MfgToolMotions](ManufacturingInterfaces/interface_MfgToolMotions_42584.md)

## Enumerated Types Index

  * [CatManufacturingPrecedenceType](ManufacturingInterfaces/enum_CatManufacturingPrecedenceType_188280.md)

---

# CatManufacturingPrecedenceType (Enumeration)

**_Possible types of precedence._**

**Values:**

` catPrecedenceTypeJustBefore`      The precedence type is JustBefore. No other element can be inserted between the 2 elements.
` catPrecedenceTypeBefore`      The precedence type is Before. Other elements can be inserted between the 2 elements.

---

# MachiningProcess (Object)

**_MachiningProcess defines a set of properties and methods to apply a Machining Process to a geometrical feature (design or manufacturing)._**
It refers to a Machining Process which has been defined in the Machining Process view of a CATProcess file In the VB macro, be sure that the **active document** is the **target document** where are located the insertion level and where the instantiated activities will be created

## Properties

### Property **InsertionLevel**( ) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   This property defines the insertion level in the program receiving the resulting operations. It can be set to either the Manufacturing Program or one the Manufacturing Activities of the Manufacturing Program.

**Example:**     The following example sets the `InsertionLevel` property to the first Manufacturing Program as `ManufacturingActivity` Activity for the mpReference `MachiningProcess` which will be used for the Machining Process application:

```VBScript
     ...
     Dim programReference As ManufacturingActivity
     Set programReference = ...
     Dim mpReference As MachiningProcess
     Set mpReference = ...
     mpReference.InsertionLevel = programReference

```

Methods

### Func **GetActivities**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)

   This method gets the Manufacturing Activities referenced by the Machining Process.

**Parameters:**

` oMfgActivities`      The Manufacturing Activities list

### Func **InsertActivity**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iActivityType`,  [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iReferencedActivity`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   This method creates and inserts a Manufacturing Activity in the Machining Process.

**Parameters:**

` iActivityType`      The activity to be created type
` iReferencedActivity`      The insertion level in the machining process: the machining process itself to insert at the beginning of the Machining Process
` oManufacturingActivity`      The inserted activity

**Example:**     The following example executes the `InsertActivity` method to add a drilling operation to the mpReference `MachiningProcess`

```VBScript
     ...
     Dim mpReference As MachiningProcess
     Set mpReference = ...
     ...
     Dim iActivityType As CATBSTR
     Set iActivityType = Drilling
     Dim iReferencedActivity As CATIAManufacturingActivity
     Set iReferencedActivity = MachiningProcess
     Dim oManufacturingActivity As CATIAManufacturingActivity
     mpReference.InsertActivity(iActivityType,iReferencedActivity,oManufacturingActivity)

```

### Sub **Instantiate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeature`)

   This method enables to apply a Machining Process to an any feature. This one has to be available for all Manufacturing Activities inside the Machining Process. At the end of the Machining Process application, the InsertionLevel property is set to the last created Manufacturing Activity in the Manufacturing program

**Example:**     The following example executes the `Instantiate` method to apply the mpReference `MachiningProcess` to a DesignFeature selected feature

```VBScript
     ...
     Dim mpReference As MachiningProcess
     Set mpReference = ...
     ...
     Dim DesignFeature As AnyObject
     Set DesignFeature = ...
     ...
     mpReference.Instantiate(DesignFeature)

```

### Sub **InstantiateInProductContext**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeature`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   This method enables to apply a Machining Process to a given feature by taking into account the product from which it belongs to. This one has to be available for all Manufacturing Activities inside the Machining Process. At the end of the Machining Process application, the InsertionLevel property is set to the last created Manufacturing Activity in the Manufacturing program

**Parameters:**

` iFeature`      The feature on which the Machining Process is instantiated
` iProduct`      The product containing the feature.

**Example:**     The following example executes the `Instantiate` method to apply the mpReference `MachiningProcess` to a iDesignFeature selected feature

```VBScript
     ...
     Dim mpReference As MachiningProcess
     Set mpReference = ...
     ...
     Dim iDesignFeature As AnyObject
     Set iDesignFeature = ...
     ...
     Dim iProduct As Product
     Set iProduct = ...
     ...
     mpReference.Instantiate(iDesignFeature,iProduct)

```

---

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

---

# ManufacturingAPTGenerator (Object)

**_Generator of APT output machining code._**

**See also:**      [ManufacturingOutputGenerator](../ManufacturingInterfaces/interface_ManufacturingOutputGenerator_169508.md)

---

# ManufacturingCopyTransformation (Object)

**_Interface representing the Manufacturing Copy Transformation object._**

**Role** : Component that implements CATIAManufacturingCopyOrder is MfgCopyOrder. This interface allows to modify the Copy Tranformation and to get the start and end points of the computed trajectory.

## Methods

### Sub **AddOperation**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iManufacturingActivity`)

   Add a Manufacturing Operation to a Copy Transformation.

**Example:**     The following example adds a manufacturing operation `myOperation`, as a reference for the Copy Transformation `CopyTransformation`

```VBScript
     call myOperation.AddOperation(CopyTransformation)

```

### Sub **GetTrajectoryEndPointCoord**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oEndPoint`)

   Retrieves the Manufacturing Copy Order trajectory end point.

**Example:**     The following example retrieves in `oEndPoint` the end point of the Manufacturing Copy Order `CopyOrder`

```VBScript
     Dim oEndPoint(3)
     call CopyOrder.GetTrajectoryEndPointCoord(oEndPoint)
     x = oEndPoint(0)
     y = oEndPoint(1)
     z = oEndPoint(2)

```

### Sub **GetTrajectoryStartPointCoord**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oStartPoint`)

   Retrieves the Manufacturing Copy Order Operation's trajectory start point.

**Example:**     The following example retrieves in `oStartPoint` the start point of the Machining Operation `Operation`

```VBScript
     Dim oStartPoint(3)
     call Operation.GetTrajectoryStartPointCoord(oStartPoint)
     x = oStartPoint(0)
     y = oStartPoint(1)
     z = oStartPoint(2)

```

### Sub **SetCopyTransformation**( long  `iNumberOfCopies`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iOrdering`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTransformationType`)

   Set the 'Number of Copies', 'Ordering' and 'Transformation Type' of a Copy Tranformation.

**Parameters:**

` iOrdering`      **Legal values** : iOrdering can be

`"EachOperationNTime"`      `"AllOperationsNTime"`
` iTransformationType`      **Legal values** : iTransformationType can be

`"Translation"`      `"Rotation"`      `"Mirror"`      `"AxisToAxis"`      `"Scale"`      `"Affinity"`      `"Matrix"`      **Example:**     The following example does that for the Copy Transformation `CopyTransformation` :

```VBScript
     call CopyTransformation.SetCopyTransformation(iNumberOfCopies, "EachOperationNTime", "Translation")

```

### Sub **SetCopyTransformationTranslationAttributes**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTranslationType`,  double  `iDistanceAlongX`,  double  `iDistanceAlongY`,  double  `iDistanceAlongZ`)

   Set the 'Translation Type', 'Distance Along X', 'Distance Along Y' and 'Distance Along Z' of a Copy Tranformation which has a Translation as transformation.

**Parameters:**

` iTranslationType`      **Legal values** : iTranslationType can be

`"AbsoluteCoordinates"`      `"CurrentCoordinates"`
` iDistanceAlongX`      distance along X in mm.
` iDistanceAlongY`      distance along Y in mm.
` iDistanceAlongZ`      distance along Z in mm. **Example:**     The following example does that for the Copy Transformation `CopyTransformation` :

```VBScript
     call CopyTransformation.SetCopyTransformationTranslationAttributes("AbsoluteCoordinates", 0.0, 100.0, 0.0)

```

---

# ManufacturingFeature (Object)

**_ManufacturingFeature defines a set of methods to access a Manufacturing Feature._**

## Methods

### Func **GetAGeometricAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve a geometry attribute of a Manufacturing Feature from its name.

**Parameters:**

` iAttribute`      The identifier of the attribute to be read **Example:**     The following example retrieves the attribute 'MfgHoleExtension' of the manufacturing feature `mfgFeature`:

```VBScript
     call mfgFeature.GetAGeometricAttribute('MfgHoleExtension' ,ExtentParm)

```

---

# ManufacturingFeatures (Collection)

**_Collection of Manufacturing Features._**

**See also:**      [ManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

   Create and Add a Manufacturing Feature of a specified type to the Collection.

**Example:**     The following example creates and adds in `Features` the manufacturing feature `Feature` of type : `type`

```VBScript
     Set Feature = Features.Add(Type)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

   Retrieve the Manufacturing Feature of a the specified index from the Collection.

**Example:**     The following example retrieves from `Feature` the manufacturing feature `Feature` from index : `Index`

```VBScript
     Set Feature = Features.Item(Index)

```

---

# ManufacturingGeneratorData (Object)

**_Represents the manufacturing output stream object._**
This object contains the output stream generated for the output files (APT, etc.).

## Methods

### Sub **AddObjectToGenerate**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

   Adds an object to the output stream.

  * With buffer: V5R13 and next <=> AddObjectToGenerate
  * Without buffer: V5R12 and previous <=> AddObjectToGenerate
  * From buffer: Debug only

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToGenerateFromBuffer**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

   Adds an object to the output stream from the buffer.

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToGenerateWithBuffer**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

   Adds an object to the output stream within the buffer.

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToGenerateWithOutBuffer**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

   Adds an object to the output stream without the buffer.

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToModalValues**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

   Adds an object to the modal values manager only.

**Parameters:**

` iObject`      The object to add

### Sub **GetFT06Stream**( [CATIAManufacturingOutput](../ManufacturingInterfaces/interface_ManufacturingOutput_79839.md)  `oStream`)

   Retrieves the FT06 stream.

**Parameters:**

` oStream`      The retrieved stream

### Sub **GetLastObjectToGenerate**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `oObject`)

   Retrieves the last object to generate.

**Parameters:**

` oObject`      The retrieved object

### Sub **GetOutputStream**( [CATIAManufacturingOutput](../ManufacturingInterfaces/interface_ManufacturingOutput_79839.md)  `oStream`)

   Retrieves the output stream.

**Parameters:**

` oStream`      The retrieved stream

### Sub **ResetAllModalValues**( )

   Resets all modal values.  
### Sub **SetLastObjectToGenerate**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

   Sets the last Activity to generate.

**Parameters:**

` iObject`      The activity to generate

---

# ManufacturingHole (Object)

**_Hole Feature in Machining domain._**

## Properties

### Property **Depth**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole depth.

**Returns:**      oDepth A CATIALength object controlling the hole depth (@see CATIALength for more information)

**Example:**     The following example returns in `holeDepth` the depth of hole `firstHole`:

```VBScript
     Set holeDepth = firstHole.Depth

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole diameter.

**Returns:**      oDiameter A CATIALength object controlling the hole diameter (@see CATIALength for more information)

**Example:**     The following example returns in `holeDiam` the diameter of hole `firstHole`:

```VBScript
     Set holeDiam = firstHole.Diameter

```

Methods

### Sub **GetDirection**( double  `oX`,  double  `oY`,  double  `oZ`)

   Returns the hole direction with absolute coordinates.

**Returns:**      3 doubles: X, Y, Z - direction coordinates

**Example:**     The following example returns in `X, Y, Z` the direction coordinates of hole `firstHole`:

```VBScript
     call firstHole.GetDirection(X,Y,Z)

```

### Sub **GetOrigin**( double  `oX`,  double  `oY`,  double  `oZ`)

   Returns the origin point which the hole is anchored to.

**Returns:**      3 doubles: X, Y, Z - Hole origin point coordinates

**Example:**     The following example returns in `X, Y, Z` the origin coordinates of hole `firstHole`:

```VBScript
     call firstHole.GetOrigin(X,Y,Z)

```

---

# ManufacturingInsert (Object)

**_The interface to access a CATIAManufacturingInsert._**

## Properties

### Property **InsertType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the technological type of a the insert. Example: The following example return the insert type theType of to the insert CurrentInsert theType=CurrentInsert.InsertType.  
### Property **NumberOfAttributes**( ) As short (Read Only)

   Give the Number of attributes of an insert object. Example: The following example returns the Number of attributes of the insert object CurrentInsert. Number = CurrentInsert.NumberOfAttributes.  Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve by is name the attribute of an insert object. Each attribute is a CKE object. Example: The following example retreives in MachiningQuality the attribute MfgMachiningQuality of the insert CurrentInsert

```VBScript
     Set MachiningQuality = CurrentInsert.GetAttribute(MfgMachiningQuality).

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iAttributName) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

     Gives the NLS value of an insert object
     Example:
     The following example gives in NLSresult the NLS value of the "MFG_COMMENT" attributes
     of the insert CurrentInsert
     NLSresult = CurrentInsert.GetAttributeNLSName("MFG_COMMENT").

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  oListOfAttributeUnits)

     Retrieve the list of attribute units of an insert object.
     The number of items in the output array is equal to the number of attributes of the insert.
     When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.
     Example:
     The following example retrieves in TabAttributeUnits the list of attribute units
     of the insert object CurrentInsert
     call CurrentInsert.GetListOfAttributeUnits(TabAttributeUnits).

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  oListOfAttributes)

     Retrieve the list of attributes of an insert object.
     Each attribute is returned as the name of a CKE object.
     Example:
     The following example retrieves in TabAttributes the list of attributes
     of the insert object CurrentInsert
     call CurrentInsert.GetListOfAttributes(TabAttributes).

---

# ManufacturingMachinableArea (Object)

**_Machinable Area in Manufacturing._**
It is a manufacturing feature pointing design features through one or several machinable geometry. This manufacturing feature could be a target for a manufacturing activity.

**See also:**      [ManufacturingMachinableGeometry](../ManufacturingInterfaces/interface_ManufacturingMachinableGeometry_202868.md), [ManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

## Properties

### Property **Freezed**( ) As boolean

   Returns the manufacturing machinable area freezed state.

**Returns:**      oFreezed The manufacturing machinable area freezed state  **Example:**     The following example returns in `bFreezed` the freezed state of manufacturing machinable area `firstMachArea`:

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim bFreezed As boolean
     Set bFreezed = firstMachArea.Freezed

```

### Property **VisibleInMfgView**( ) As boolean

   Returns the manufacturing machinable area visibility state.

**Returns:**      oVisibleInMfgView The manufacturing machinable area visibility state  **Example:**     The following example returns in `bVisibleInMfgView` the visible state in the Manufacturing View of manufacturing machinable area `firstMachArea`:

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim bVisibleInMfgView As boolean
     Set bVisibleInMfgView = firstMachArea.VisibleInMfgView

```

Methods

### Sub **AddMachinableGeometry**( [CATIAManufacturingMachinableFeat](../ManufacturingInterfaces/interface_ManufacturingMachinableFeature_187924.md)  `iMachinableGeometry`)

   Adds a machinable geometry to the list.

**Parameters:**

` iMachinableGeometry`      The machinable geometry to affect  **Example:**     The following example adds the machinable geometry `MachGeomToAdd` to the manufacturing machinable area `firstMachArea`.

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim MachGeomToAdd As ManufacturingMachinableGeometry
     Set MachGeomToAdd = ...
     Call firstMachArea.AddMachinableGeometry( MachGeomToAdd )

```

### Sub **ListMachinableGeometry**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfMachinableGeometry`)

   Retrieves the machinable geometry list.

**Parameters:**

` oListOfMachinableGeometry`      The retrieved list.
The array must be previously initialized using the
MachinableGeometryCount method.  **Example:**     The following example retrieves the machinable geometry list of the manufacturing machinable area `firstMachArea` in `MachinableGeometryList`.

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim MachinableGeometryListSize As Long
     Set MachinableGeometryListSize = firstMachArea.MachinableGeometryCount
     If MachinableGeometryListSize > 0 Then
       Dim MachinableGeometryList() As Variant
       Redim MachinableGeometryList(MachinableGeometryListSize-1)
       Call firstMachArea.ListMachinableGeometry(MachinableGeometryList)
     End If

```

### Sub **ListManufacturingActivityConnected**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfManufacturingActivityConnected`)

   Retrieves the manufacturing activity connected list.

**Parameters:**

` oListOfManufacturingActivityConnected`      The retrieved list.
The array must be previously initialized using the
ManufacturingActivityConnectedCount method.  **Example:**     The following example retrieves the manufacturing activity connected list of the manufacturing machinable area `firstMachArea` in `ManufacturingActivityConnectedList`.

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim ManufacturingActivityConnectedListSize As Long
     Set ManufacturingActivityConnectedListSize = firstMachArea.ManufacturingActivityConnectedCount
     If ManufacturingActivityConnectedListSize > 0 Then
       Dim ManufacturingActivityConnectedList() As Variant
       Redim ManufacturingActivityConnectedList(ManufacturingActivityConnectedListSize-1)
       Call firstMachArea.ListManufacturingActivityConnected(ManufacturingActivityConnectedList)
     End If

```

### Func **MachinableGeometryCount**( ) As long

   Returns the machinable geometry list count.

**Parameters:**

` oMachinableGeometryCount`      The number of machinable geometry connected to this feature  **Example:**     The following example retrieves the machinable geometry list count of the manufacturing machinable area `firstMachArea` in `MachinableGeometryListSize`.

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim MachinableGeometryListSize As Long
     Set MachinableGeometryListSize = firstMachArea.MachinableGeometryCount

```

### Func **ManufacturingActivityConnectedCount**( ) As long

   Returns the manufacturing activity connected list count.

**Parameters:**

` oManufacturingActivityConnectedCount`      The number of manufacturing activity pointing this feature  **Example:**     The following example retrieves the manufacturing activity connected list count of the manufacturing machinable area `firstMachArea` in `ManufacturingActivityConnectedListSize`.

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim ManufacturingActivityConnectedListSize As Long
     Set ManufacturingActivityConnectedListSize = firstMachArea.ManufacturingActivityConnectedCount

```

### Sub **RemoveMachinableGeometry**( [CATIAManufacturingMachinableFeat](../ManufacturingInterfaces/interface_ManufacturingMachinableFeature_187924.md)  `iMachinableGeometry`)

   Removes a machinable geometry from the list.

**Parameters:**

` iMachinableGeometry`      The machinable geometry to remove  **Example:**     The following example removes the machinable geometry `MachGeomToRemove` to the manufacturing machinable area `firstMachArea`.

```VBScript
     Dim firstMachArea As ManufacturingMachinableArea
     Set firstMachArea = ...
     Dim MachGeomToRemove As ManufacturingMachinableGeometry
     Set MachGeomToRemove = ...
     Call firstMachArea.RemoveMachinableGeometry( MachGeomToRemove )

```

---

# ManufacturingMachinableFeature (Object)

**_Machinable Feature in Manufacturing._**
It is the base object for machinable geometry and machinable area

**See also:**      [ManufacturingMachinableArea](../ManufacturingInterfaces/interface_ManufacturingMachinableArea_149911.md), [ManufacturingMachinableGeometry](../ManufacturingInterfaces/interface_ManufacturingMachinableGeometry_202868.md)

## Properties

### Property **FeatRemark**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the manufacturing machinable feature remark.

**Returns:**      oFeatRemark The manufacturing machinable feature remark  **Example:**     The following example returns in `tFeatRemark` the remark of manufacturing machinable feature `firstMachFeat`:

```VBScript
     Dim firstMachFeat As ManufacturingMachinableFeature
     Set firstMachFeat = ...
     Dim tFeatRemark As CATBSTR
     Set tFeatRemark = firstMachFeat.FeatRemark

```

### Property **FeatType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the manufacturing machinable feature type.

**Returns:**      oFeatType The manufacturing machinable feature type  **Example:**     The following example returns in `tFeatType` the type of manufacturing machinable feature `firstMachFeat`:

```VBScript
     Dim firstMachFeat As ManufacturingMachinableFeature
     Set firstMachFeat = ...
     Dim tFeatType As CATBSTR
     Set tFeatType = firstMachFeat.FeatType

```

---

# ManufacturingMachinableGeometry (Object)

**_Represents the machinable geometry object._**
It is the low-level component of a machinable area.

**See also:**      [ManufacturingMachinableArea](../ManufacturingInterfaces/interface_ManufacturingMachinableArea_149911.md)

## Properties

### Property **Shared**( ) As boolean

   Returns or sets the shared state of a ManufacturingMachinableGeometry object.  **Example:**     The following example returns in `bState` the shared state of manufacturing machinable geometry `firstMachGeom` and then sets it to TRUE:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim bState As boolean
     Set bState = firstMachGeom.Shared
     bState = TRUE
     firstMachGeom.Shared = bState

```

Methods

### Sub **AddPointedGeometry**( [CATIABase](../System/interface_AnyObject_17321.md)  `iGeometry`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iShapes`)

   Adds a geometry to the pointed geometry list.

**Parameters:**

` iGeometry`      The geometry to add
` iProduct`      The product where the geometry to add is located
` iShapes`      The list of shapes (body copied and pasted with links) where the geometry is to be added  **Example:**     The following example adds the geometry `GeomToAdd` of the product `ProdOfGeomToAdd` to the pointed geometry list of the manufacturing machinable geometry `firstMachGeom`.

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim GeomToAdd As Shape
     Dim ProdOfGeomToAdd As Product
     Set GeomToAdd = ...
     Set ProdOfGeomToAdd = ...
     Dim ShapesList() As Variant
     Redim ShapesList(0) ' Create an empty list of shapes
     Call firstMachGeom.AddPointedGeometry( GeomToAdd, ProdOfGeomToAdd, ShapesList )

```

### Sub **AddPointedGeometryNotify**( [CATIABase](../System/interface_AnyObject_17321.md)  `iGeometry`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iShapes`,  short  `iNotify`)

   Adds a geometry to the pointed geometry list (manage notification).

**Parameters:**

` iGeometry`      The geometry to add
` iProduct`      The product where the geometry to add is located
` iShapes`      The list of shapes (body copied and pasted with links) where the geometry is to be added
` iNotify`      A flag to request whether to send a notification to update the model

**Legal values** :  | **0** | No notification is sent and the model is not updated
---|---

**1** | A notification is sent and the model is updated

**Example:**     The following example adds the geometry `GeomToAdd` of the product `ProdOfGeomToAdd` to the pointed geometry list of the manufacturing machinable geometry `firstMachGeom`.

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim GeomToAdd As Shape
     Dim ProdOfGeomToAdd As Product
     Set GeomToAdd = ...
     Set ProdOfGeomToAdd = ...
     Dim ShapesList() As Variant
     Redim ShapesList(0) ' Create an empty list of shapes
     Call firstMachGeom.AddPointedGeometryNotify( GeomToAdd, ProdOfGeomToAdd, ShapesList, 0 )

```

### Sub **AddPointedGeometryWithNoDuplicatedCheck**( [CATIABase](../System/interface_AnyObject_17321.md)  `iGeometry`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iShapes`)

   Adds a geometry to the pointed geometry list with no check on already referenced geometry.

**Parameters:**

` iGeometry`      The geometry to add
` iProduct`      The product where the geometry to add is located
` iShapes`      The list of shapes (body copied and pasted with links) where the geometry is to be added  **Example:**     The following example adds the geometry `GeomToAdd` of the product `ProdOfGeomToAdd` to the pointed geometry list of the manufacturing machinable geometry `firstMachGeom`.

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim GeomToAdd As Shape
     Dim ProdOfGeomToAdd As Product
     Set GeomToAdd = ...
     Set ProdOfGeomToAdd = ...
     Dim ShapesList() As Variant
     Redim ShapesList(0) ' Create an empty list of shapes
     Call firstMachGeom.AddPointedGeometryWithNoDuplicatedCheck( GeomToAdd, ProdOfGeomToAdd, ShapesList )

```

### Sub **AddPointedGeometryWithNoDuplicatedCheckNotify**( [CATIABase](../System/interface_AnyObject_17321.md)  `iGeometry`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iShapes`,  short  `iNotify`)

   Adds a geometry to the pointed geometry list with no check on an already referenced geometry.

**Parameters:**

` iGeometry`      The geometry to add
` iProduct`      The product where the geometry to add is located
` iShapes`      The list of shapes (body copied and pasted with links) where the geometry is to be added
` iNotify`      A flag to request whether to send a notification to update the model

**Legal values** :  | **0** | No notification is sent and the model is not updated
---|---

**1** | A notification is sent and the model is updated

**Example:**     The following example adds the geometry `GeomToAdd` of the product `ProdOfGeomToAdd` to the pointed geometry list of the manufacturing machinable geometry `firstMachGeom`:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim GeomToAdd As Shape
     Dim ProdOfGeomToAdd As Product
     Set GeomToAdd = ...
     Set ProdOfGeomToAdd = ...
     Dim ShapesList() As Variant
     Redim ShapesList(0) ' Create an empty list of shapes
     Call firstMachGeom.AddPointedGeometryWithNoDuplicatedCheckNotify( GeomToAdd, ProdOfGeomToAdd, ShapesList, 0 )

```

### Sub **GetAssociatedTPS**( long  `IndexOfPointedGeom`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAnnotationsList`)

   Retrieves the Annotation object lists associated with a ManufacturingMachinableGeometry object.

**Parameters:**

` IndexOfPointedGeom`      The index of the pointed geometry among those associated with the ManufacturingMachinableGeometry object
` oAnnotationsList`      The retrieved list Annotation objects.
The array must be previously initialized using the
GetAssociatedTPSCount method.  **Example:**     The following example retrieves the Annotation object list of the third pointed geometry under the manufacturing machinable geometry `firstMachGeom` in `AnnotationList`:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim AssociatedTPSCount As Long
     AssociatedTPSCount = firstMachGeom.GetAssociatedTPSCount (2)
     If (AssociatedTPSCount > 0) Then
       Dim I As Long

       Dim AnnotationList() As Variant
       Redim AnnotationList(AssociatedTPSCount-1)
       Call firstMachGeom.GetAssociatedTPS(2, AnnotationList)

     End If

```

### Func **GetAssociatedTPSCount**( long  `IndexOfPointedGeom`) As long

   Returns the number of Annotation objects attached to a pointed geometry under a ManufacturingMachinableGeometry object.

**Parameters:**

` IndexOfPointedGeom`      The index of the pointed geometry

**Note** : Check that the index you are passing in less than or equal to the pointed geometry count retrieved using the
PointedGeometryCount method. ` oAnnotationsListCount`      The number of Annotation objects  **Example:**     The following example retrieves the number of Annotation objects attached to the third geometry under the manufacturing machinable geometry `firstMachGeom` in `AssociatedTPSCount`:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim AssociatedTPSCount As Long
     AssociatedTPSCount = PointedGeometryListSize = firstMachGeom.GetAssociatedTPSCount( 3 )

```

### Sub **GetDirection**( double  `oX`,  double  `oY`,  double  `oZ`,  long  `IndexOfPointedGeom`)

   Retrieves the direction of a pointed geometry under a ManufacturingMachinableGeometry object.

**Note** : Currently valid only for AxialUDF and DesignHole features.

**Parameters:**

` oX,oY,oZ`      The components of the direction
` IndexOfPointedGeom`      The index of the pointed geometry

**Note** : Check that the index you are passing in less than or equal to the pointed geometry count retrieved using the
PointedGeometryCount method.  **Example:**     The following example retrieves the components of the direction of the third geometry under the manufacturing machinable geometry `firstMachGeom`:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim oX As Double
     Dim oY As Double
     Dim oZ As Double
     Call firstMachGeom.GetDirection( oX, oY, oZ, 3)

```

### Sub **GetOrigin**( double  `oX`,  double  `oY`,  double  `oZ`,  long  `IndexOfPointedGeom`)

   Retrieves the origin of a pointed geometry under a ManufacturingMachinableGeometry object.

**Note** : Currently valid only for AxialUDF and DesignHole features.

**Parameters:**

` oX,oY,oZ`      The coordinates of the origin
` IndexOfPointedGeom`      The index of the pointed geometry

**Note** : Check that the index you are passing in less than or equal to the pointed geometry count retrieved using the
PointedGeometryCount method.  **Example:**     The following example retrieves the coordinates of the origin of the third geometry under the manufacturing machinable geometry `firstMachGeom`:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim oX As Double
     Dim oY As Double
     Dim oZ As Double
     Call firstMachGeom.GetOrigin( oX, oY, oZ, 3)

```

### Sub **ListPointedGeometry**( long  `iIndex`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oGeometry`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `oProduct`,  long  `oNbShapes`)

   Retrieves a pointed geometry and its product.

**Parameters:**

` iIndex`      The index of the pointed geometry and product
` oGeometry`      The retrieved geometry
` oProduct`      The product of the retrieved geometry
` oNbShapes`      The number of shapes of the retrieved geometry  **Example:**     The following example retrieves the pointed geometry lists of the manufacturing machinable geometry `firstMachGeom` in `PointedGeometryList` and in `PointedProductsList`. The arrays must be previously initialized using the
PointedGeometryCount method.

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim PointedGeometryListSize As Long
     Set PointedGeometryListSize = firstMachGeom.PointedGeometryCount
     If (PointedGeometryListSize > 0) Then
       Dim I As Long
       For I = 0 To PointedGeometryListSize-1
         Dim PointedGeometryList() As Variant
         Dim PointedProductsList() As Variant
         Dim NbShapes As Long
         Redim PointedGeometryList(PointedGeometryListSize-1)
         Redim PointedProductsList(PointedGeometryListSize-1)
         Call firstMachGeom.ListPointedGeometry(I, PointedGeometryList, PointedProductsList, NbShapes)
       End For
     End If

```

### Sub **ListShapesOfPointedGeometry**( long  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oShapes`)

   Retrieves the pointed shape list.

**Parameters:**

` iIndex`      The index of the pointed geometry and product
` oShapes`      The retrieved shape list.
The array must be previously initialized using the
ListPointedGeometry method.  **Example:**     The following example retrieves the pointed shape list of the manufacturing machinable geometry `firstMachGeom` in `PointedShapesList`.

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim PointedGeometryListSize As Long
     Set PointedGeometryListSize = firstMachGeom.PointedGeometryCount
     If (PointedGeometryListSize > 0) Then
       Dim I As Long
       For I = 0 To PointedGeometryListSize-1
         Dim PointedGeometryList() As Variant
         Dim PointedProductsList() As Variant
         Dim NbShapes As Long
         Redim PointedGeometryList(PointedGeometryListSize-1)
         Redim PointedProductsList(PointedGeometryListSize-1)
         Call firstMachGeom.ListPointedGeometry(I, PointedGeometryList, PointedProductsList, NbShapes)
         If (NbShapes > 0) Then
           Dim PointedShapesList() As Variant
           Redim PointedShapesList(NbShapes-1)
           Call firstMachGeom.ListShapesOfPointedGeometry(I, PointedShapesList)
         End If
       End For
     End If

```

### Func **PointedGeometryCount**( ) As long

   Returns the pointed geometry list count.  **Example:**     The following example retrieves the pointed geometry list count of the manufacturing machinable geometry `firstMachGeom` in `PointedGeometryListSize`.

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Dim PointedGeometryListSize As Long
     Set PointedGeometryListSize = firstMachGeom.PointedGeometryCount

```

### Sub **RemovePointedGeometry**( long  `iIndex`)

   Removes a geometry from the pointed geometry list.

**Parameters:**

` iIndex`      The index of the geometry to remove  **Example:**     The following example removes the third geometry from the pointed geometry list of the manufacturing machinable geometry `firstMachGeom`:

```VBScript
     Dim firstMachGeom As ManufacturingMachinableGeometry
     Set firstMachGeom = ...
     Call firstMachGeom.RemovePointedGeometry( 3 )

```

---

# ManufacturingMachine (Object)

**_Machine in machining domain._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the Comment of a Machine.

**Example:**     The following example return the comment `MachineComment` of to the manufacturing Machine `CurrentMachine`

```VBScript
     MachineComment = CurrentMachine.Comment

```

### Property **MachineType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the Type of a Machine.

**Example:**     The following example return the type `MachineType` of to the manufacturing Machine `CurrentMachine`

```VBScript
     MachineType = CurrentMachine.Type

```

### Property **NumberOfAttributes**( ) As short (Read Only)

   Gives the number of attributes of a ManufacturingMachine.

**Example:**     The following example returns the `Number` of attributes of the ManufacturingMachine `CurrentMachine`

```VBScript
     Number = CurrentMachine.NumberOfAttributes

```

### Property **NumberOfNumericalControlAttributes**( ) As short (Read Only)

   This property returns the number of Numerical Control attributes of a Manufacturing Machine.  
### Property **NumberOfRotaryTableAttributes**( ) As short (Read Only)

   This property returns the number of rotary table attributes of a Manufacturing Machine. The machine is upposed to accept Rotary table (type is Mfg3AxisWithTableRotationMachine).  
### Property **NumberOfSpindleAttributes**( ) As short (Read Only)

   This property returns the number of Spindle attributes of a Manufacturing Machine.  
### Property **NumberOfToolChangeAttributes**( ) As short (Read Only)

   This property returns the number of Tool change attributes of a Manufacturing Machine.  
### Property **PPTableName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Give the PPTableName linked to a Manufacturing Machine.

**Example:**     The following example returns the PPTableName `ThisPPTable` linked to the Manufacturing Machine `CurrentMachine`

```VBScript
     Set ThisPPTable = CurrentMachine.PPTableName

```

### Property **PostProcessorFile**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   This property returns the post processor file of a Manufacturing Machine Machine.PostProcessorFile  
### Property **PreferedToolCatalogName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Give the PreferedToolCatalogName linked to a Manufacturing Machine.

**Example:**     The following example returns the PreferedToolCatalogName `ThisCatalog` linked to the Manufacturing Machine `CurrentMachine`

```VBScript
     Set ThisCatalog = CurrentMachine.PreferedToolCatalogName

```

### Property **RotaryAxis**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Give the MfgRotaryAxis linked to a Manufacturing Machine.

**Example:**     The following example returns the MfgRotaryAxis `ThisAxis` linked to the Manufacturing Machine `CurrentMachine`

```VBScript
     Set ThisAxis = CurrentMachine.RotaryAxis

```

Methods

### Func **DefaultName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Return the string the Type of a Machine.

**Example:**     The following example return the type `MachineType` of to the manufacturing Machine `CurrentMachine`

```VBScript
     MachineType = CurrentMachine.Type

```

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve the Attribute of a Manufacturing Machine.

**Example:**     The following example retreives in `HomePosX` the attribute `MFG_HOME_POS_X` of Manufacturing Machine `MyMachine`

```VBScript
      Set HomePosX = MyMachine.GetAttribute(MFG_HOME_POS_X)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieve the NLS name from the attribute name of a Manufacturing Machine.

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributeUnits`)

   Retrieve the list of attribute units of a ManufacturingMachine.
The number of items in the output array is equal to the number of attributes of the machine.
When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.

**Example:**     The following example retrieves in `TabAttributeUnits` the list of attribute units of the ManufacturingMachine `CurrentMachine`

```VBScript
     call CurrentMachine.GetListOfAttributeUnits(TabAttributeUnits)

```

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of all attributes of a ManufacturingMachine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `TabAttributes` the list of attributes of the ManufacturingMachine `CurrentMachine`

```VBScript
     call CurrentMachine.GetListOfAttributes(TabAttributes)

```

### Sub **GetListOfNumericalControlAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of Numerical Control attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Numerical Control attributes of the Manufacturing Machine `myMachine`

```VBScript
     call myMachine.GetListOfNumericalControlAttributes(oListOfAttributes)

```

### Sub **GetListOfRotaryTableAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of Rotary table attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Tool Change attributes of the Manufacturing Machine `myMachine`

```VBScript
     call myMachine.GetListOfRotaryTableAttributes(oListOfAttributes)

```

### Sub **GetListOfSpindleAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of Spindle attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Spindle attributes of the Manufacturing Machine `myMachine`

```VBScript
     call myMachine.GetListOfSpindleAttributes(oListOfAttributes)

```

### Sub **GetListOfToolChangeAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of Tool Change attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Tool Change attributes of the Manufacturing Machine `myMachine`

```VBScript
     call myMachine.GetListOfToolChangeAttributes(oListOfAttributes)

```

### Sub **set_DefaultValues**( )

   Initialise the Manufacturing Machine parameters.

**Example:**     The following example make the init of the parameter of the Machine `ThisMachine` .

```VBScript
     call ThisMachine.set_DefaultValues

```

---

# ManufacturingMachiningAxis (Object)

**_ManufacturingMachiningAxis defines a set of methods to manage a Machining Axis System or an Origin._**

## Properties

### Property **Origin**( ) As short

   This property returns the interface which manages if instruction os used as an Origin or as a Machining Axis System. If instruction is an Origin, Origin is set to 1, 0 otherwise.

**Example:**     The following example returns in `origin` the attribute to provide if instruction is used as a Machining Axis System or an Origin :

```VBScript
     ...
     Set myInstruction  = ...
     Set MyOrigin = myInstruction.Origin

```

### Property **OriginGroup**( ) As short

   This property returns the interface which determines the origin group of the instruction if used a an Origin.

**Example:**     The following example set the Origin Group to 5.

```VBScript
     ...
     Set myInstruction  = ...
     Set myInstruction.OriginGroup = 3

```

### Property **OriginNumber**( ) As short

   This property returns the interface which manages the origin number of the instruction if used a an Origin.

**Example:**     The following example set the Origin Number to 3.

```VBScript
     ...
     Set myInstruction  = ...
     Set myInstruction.OriginNumber = 3

```

Methods

### Sub **GetOriginPoint**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with PointOrigin as an Origin Point and with ProductOrigin a belonging product.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     Dim PointOrigin As CATSafeArrayVariant
     Dim ProductOrigin As Product
     MfgAxisSystem.GetOriginPoint (PointOrigin)

```

### Sub **GetOriginXDirection**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin X direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with origin X direction in DblMathDirection.

```VBScript
     Dim DlbMathDirection As Double(3)
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.GetOriginXDirection (DblMathDirection)

```

### Sub **GetOriginYDirection**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin Y direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with origin Y direction in DblMathDirection.

```VBScript
     Dim DlbMathDirection As Double(3)
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.GetOriginYDirection (DblMathDirection)

```

### Sub **GetOriginZDirection**( double  `x`,  double  `y`,  double  `z`)

   Gets the Origin Z direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example gets `MfgAxisSystem` with origin Z direction in DblMathDirection.

```VBScript
     Dim x,y,z As Double
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.GetOriginZDirection (x,y,z)

```

### Sub **SetOriginPoint**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`)

   Sets the Origin of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example sets `MfgAxisSystem` with PointOrigin as an Origin Point and with ProductOrigin a belonging product.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     Dim PointOrigin As AnyObject
     Dim ProductOrigin As Product
     MfgAxisSystem.SetOriginPoint (PointOrigin,ProductOrigin)

```

### Sub **SetOriginPointByCoordinates**( double  `x`,  double  `y`,  double  `z`)

   Sets the Origin of a Manufacturing Machining Axis System used as Origin by coordinates.

**Example:**     The following example sets the Origin `MfgAxisSystem` at coordinates x,y,z.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.SetOriginPointByCoordinates(x,y,z)

```

### Sub **SetOriginXDirection**( double  `x`,  double  `y`,  double  `z`)

   Sets the Origin X direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example sets `MfgAxisSystem` with origin X direction in DblMathDirection.

```VBScript
     Dim DlbMathDirection As Double(3)
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.SetOriginXDirection (DblMathDirection)

```

### Sub **SetOriginZDirection**( double  `x`,  double  `y`,  double  `z`)

   Sets the Origin Z direction of a Manufacturing Machining Axis System used as Origin.

**Example:**     The following example sets `MfgAxisSystem` with origin Y direction in DblMathDirection.

```VBScript
     Dim x,y,z As Double
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     MfgAxisSystem.SetOriginZDirection (x,y,z)

```

### Sub **SetPartAxisSystem**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPAS`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`)

   Sets the Part Axis System of a Manufacturing Machining Axis System.

**Example:**     The following example sets `MfgAxisSystem` with PAS as a Part Axis System and with ProductPAS a belonging product.

```VBScript
     Dim MfgAxisSystem As ManufacturingMachiningAxis
     Set MfgAxisSystem = ...
     Dim PAS As AxisSystem
     Dim PASProduct As Product
     MfgAxisSystem.SetMachiningAxisSystem (PAS,PASProduct)

```

---

# ManufacturingOperation (Object)

**_ManufacturingOperation defines a set of methods._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Return the Comment linked to a Manufacturing Operation.

**Example:**     The following example returns the Comment `ThisComment` linked to a manufacturing operation `CurrentMo`

```VBScript
     Set ThisComment = CurrentMo.Comment

```

Methods

### Sub **AddClearance**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  double  `iA`,  double  `iB`,  double  `iC`,  double  `iD`)

   Add a 'clearance to a plane' path to a Manufacturing Operation.

**Example:**     The following example add a path (clerarance) on approach macro of `operation`

```VBScript
     call Operation.AddClearance("Approach", A, B, C, D)

```

### Sub **AddDistanceAlongAlineMotion**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a path 'distance along a line' to a Manufacturing Operation.

**Example:**     The following example add a path (distance along a line) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAlineMotion("LinkingApproach", distance, iLine, iProduct)

```

### Sub **AddDistanceAlongAlineMotionFeed**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`,  double  `iFeedrateValue`)

   Add a path 'distance along a line' with Feedrate info to a Manufacturing Operation.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be

`"None"`      `"Machining"`      `"Approach"`      `"Retract"`      `"RAPID"`      `"Local"`
` iFeedrateValue`      feedrate Value in MKS units : m/s if linear feedrate, or m/turn if angular feedrate (take into account only if iFeedrateType = "Local")  **Example:**     The following example add a path (distance along a line) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAlineMotionFeed("LinkingApproach", distance, iLine, iProduct, iFeedrateType, iFeedrateValue)

```

### Sub **AddDistanceAlongAxis**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`)

   Add a path 'distance along axis' to a Manufacturing Operation.

**Example:**     The following example add a path (distance along axis) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAxis("LinkingApproach", distance)

```

### Sub **AddDistanceAlongAxisFeed**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  double  `iDistance`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`,  double  `iFeedrateValue`)

   Add a path 'distance along axis' with Feedrate info to a Manufacturing Operation.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be

`"None"`      `"Machining"`      `"Approach"`      `"Retract"`      `"RAPID"`      `"Local"`
` iFeedrateValue`      feedrate Value in MKS units : m/s if linear feedrate, or m/turn if angular feedrate (take into account only if iFeedrateType = "Local")  **Example:**     The following example add a path (distance along axis) on the approach group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddDistanceAlongAxisFeed("LinkingApproach", distance, iFeedrateType, iFeedrateValue)

```

### Sub **AddGotoHorizontal**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  double  `iDistance`,  double  `iAngle1`,  double  `iAngle2`)

   Add a path 'goto horizontal' to a Manufacturing Operation.

**Example:**     The following example add a path (goto horizontal) on approach macro of `operation`

```VBScript
     call Operation.AddGotoHorizontal("Approach", distance, angle1, angle2)

```

### Sub **AddMotionGoToAPoint**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a path 'goto a point' to a Manufacturing Operation.

**Example:**     The following example add a path (goto a point ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionGoToAPoint("Approach", iPoint, iProduct )

```

### Sub **AddMotionGoToAPointFeed**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPoint`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`,  double  `iFeedrateValue`)

   Add a path 'goto a point' with Feedrate info to a Manufacturing Operation.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be

`"None"`      `"Machining"`      `"Approach"`      `"Retract"`      `"RAPID"`      `"Local"`
` iFeedrateValue`      feedrate Value in MKS units : m/s if linear feedrate, or m/turn if angular feedrate (take into account only if iFeedrateType = "Local")  **Example:**     The following example add a path (goto a point ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionGoToAPointFeed("Approach", iPoint, iProduct, iFeedrateType, iFeedrateValue)

```

### Sub **AddMotionToAPlane**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  short  `iMode`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPlane`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a path 'goto a plane with axial or perpendicular move' to a Manufacturing Operation.

**Example:**     The following example add a path (goto a plane with axial move ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionToAPlane("Approach", 1, iPlane, iProduct)

```

**Example:**     The following example add a path (goto a plane with perpendicular move ) on approach macro of `operation`

```VBScript
     call Operation.AddMotionToAPlane("Approach", 0, iPlane, iProduct)

```

### Sub **AddPPWords**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMacro`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPPWords`)

   Add a path 'PP Words' to a Manufacturing Operation.

**Example:**     The following example add a path (PP Words) on the retract group of path of the Linking macro of `operation`

```VBScript
     call Operation.AddPPWords("LinkingRetract", "PP Words example")

```

### Func **GetAGeometricAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve a Geometric Attribute of a Manufacturing Operation.

**Example:**     The following example retrieves in `Offset` the attribute `OriginOffset` of Manufacturing Operation `firstOperation`

```VBScript
     Set Offset = firstOperation.GetAttribute(OriginOffset)

```

### Func **GetAnAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve the Attribute of a Manufacturing Operation.

**Example:**     The following example Retrieves in `RapidFeed` the attribute `MfgRapidFeed` of Manufacturing Operation `firstOperation`

```VBScript
     Set RapidFeed = firstOperation.GetAttribute(MfgRapidFeed)

```

### Func **GetFeature**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve the Machinable Feature asociated to a Manufacturing Operation.

**Example:**     The following example Retrieves in `firstOperation` the machinable feature `Feature`

```VBScript
     call firstOperation.GetFeature(Feature)

```

### Func **GetFeedSpeedAutoUpdate**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As boolean

   Returns the Auto Update status for Feed Rate or Spindle Speed.

**Parameters:**

` iType`      Determines if the method works on Feed Rate or Spindle Speed **Legal values** : iType can be

  * `"FEEDRATE"`
  * `"SPINDLESPEED"`

**Returns:**      oAutoUpdate Auto update status

  * **Example:**
  * The following example checks the status of AutoUpdate for Feed Rate
  * Dim isAutoUpdateEnabled As Boolean
  * isAutoUpdateEnabled = firstOperation.GetFeedSpeedAutoUpdate("FEEDRATE")

### Func **GetListOfToolMotions**( ) As [CATIAMfgToolMotions](../ManufacturingInterfaces/interface_MfgToolMotions_42584.md)

   Give a list of Manufacturing ToolMotion contained by a sequential operation.

See interface CATIAMfgToolMotions for methods available on the list      The following example extract the tool motions of operation SeqMO in the MfgToolMotions      list TMList2 .

```VBScript

     **Example:**
    	Dim TMList2 As MfgToolMotions
    	Set TMList2 = SeqMO.GetListOfToolMotions
    	Dim Test2 As ManufacturingToolMotion
    	Set Test2 = TMList2.GetElement(1)

```

### Func **GetManufacturingFeature**( ) As [CATIAManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

   Retrieve the Manufacturing Feature asociated to a Manufacturing Operation.

**Example:**     The following example Retrieves in `firstOperation` the manufacturing feature `Feature`

```VBScript
     Set Feature = firstOperation.GetManufacturingFeature

```

### Func **GetMfgAparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim A
     Set A = firstOperation.GetMfgBparamTopPln

```

### Func **GetMfgAxialFeatureDiameter**( ) As double

   Retrieve the diameter of an axial manufacturing feature.

**Example:**     The following example Retrieves in `Diam` the diameter of the axial manufacturing feature linked to the operation `firstOperation`

```VBScript
     Dim Diam
     Set Diam = firstOperation.GetMfgAxialFeatureDiameter

```

### Func **GetMfgBparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim B
     Set B = firstOperation.GetMfgBparamTopPln

```

### Func **GetMfgCparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim C
     Set C = firstOperation.GetMfgCparamTopPln

```

### Func **GetMfgDparamTopPln**( ) As double

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Dim D
     Set D = firstOperation.GetMfgDparamTopPln

```

### Sub **GetMfgFeaturePosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioPosition`)

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim oPositionArray(3) As CATSafeArrayVariant
     Call firstOperation.GetMfgFeaturePosition(oPositionArray)
     Assume this array is oPositionArray. It contains:

     oPositionArray[0],oPositionArray[1],oPositionArray[2]
         The X, Y, and Z direction vector components

     **Example:**
         The following example returns in oPositionArray
     the coordinates of the feature position

```VBScript
     Call firstOperation.GetMfgFeaturePosition(oCoord)
     x = oPositionArray[0]
     y = oPositionArray[1]
     z = oPositionArray[2]

```

### Func **GetMfgFeatureXPosition**( ) As double

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim X
     X = firstOperation.GetMfgFeatureXPosition

```

### Func **GetMfgFeatureYPosition**( ) As double

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim Y
     Y = firstOperation.GetMfgFeatureYPosition

```

### Func **GetMfgFeatureZPosition**( ) As double

   Retrieve the Coordinate of the Reference Point of a Drill Operation.

**Example:**     The following example Retrieves in `X,Y,Z` the coordinate (X,Y,Z) of the Reference Point of the Drill Operation `firstOperation`

```VBScript
     Dim Z
     Z = firstOperation.GetMfgFeatureZPosition

```

### Sub **GetMfgTopPlane**( double  `oA`,  double  `oB`,  double  `oC`,  double  `oD`)

   Retrieve the Equation of the Top Plane of a Pocket Operation.

**Example:**     The following example Retrieves in `A,B,C,D` the equation Ax + By + Cz + D = 0 of Manufacturing Pocket Operation `firstOperation`

```VBScript
     Call firstOperation.GetMfgTopPlane(A,B,C,D)

```

### Func **GetPattern**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve the Machining Pattern asociated to a Manufacturing Operation.

**Example:**     The following example Retrieves in `firstOperation` the machining pattern `Pattern`

```VBScript
     Set Pattern = firstOperation.GetPattern

```

### Func **GetRadiusOnMacro**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMacroType`) As double

   Retrieves radius attribute on the circular elementary macro motion on CIRCULAR MILLING or THREAD MILLING operations ONLY.

**Parameters:**

` iMacroType`      **Legal values** : iMacroType can be:

`"Approach"`, to get the radius on the Approach Macro      `"Retract"`, to get the radius on the Retract Macro      `"ReturnInALevelApproach"`, to get the radius on the Return in a level Macro (Approach)      `"ReturnInALevelRetract"`, to get the radius on the Return in a level Macro (Retract)      `"ReturnBetweenLevelsApproach"`, to get the radius on the Return between levels Macro (Approach)      `"ReturnBetweenLevelsRetract"`, to get the radius on the Return between levels Macro (Approach)
` oRadius`      Radius value. (expressed in millimeters)  **Example:**     The following example retrieves the radius on the circular motion of the retract macro on the Circular Milling operation CircularMilling1

```VBScript
     dim RadValue as double
     RadValue = CircularMilling1.GetRadiusOnMacro("Retract")

```

### Sub **GetRelimitingGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oProduct`,  double  `oOffset`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPosition`)

   Retrieves start / end element on PROFILE CONTOURING operation ONLY.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be:

`"StartElement"`, to get the Start element on Profile Contouring      `"EndElement"`, to get the End element on Profile Contouring
` oReference`      The relimiting geometry.
` oProduct`      Product containing the relimiting geometry.
` oOffset`      Offset set on the relimiting geometry. (expressed in millimeters)
` oPosition`      Tool position set on the relimiting geometry.

**Legal values** : oPosition can be:

`"IN"`     `"ON"`     `"OUT"`     **Example:**     The following example gets the End relimiting element of the Profile Contouring operation Contouring1

```VBScript
     Call Contouring1.GetRelimitingGeometry("EndElement",RelimitingElement,PartMachined,Offset,Position)

```

### Sub **GetStartPointGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oGeometryPosition`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oProduct`,  double  `oOffset`)

   Retrieves geometry and offset of a start point on POCKETING operation ONLY.

**Parameters:**

` oGeometryPosition`      **Legal values** : oGeometryPosition can be:

`"Outside"`, if the start point is outside the pocket contour      `"Inside"`, if the start point is inside the pocket contour
` oReference`      The start point geometry.
` oProduct`      Product containing the start point geometry.
` oOffset`      Offset set on the start point. (expressed in millimeters)
Offset has a meaning only if oGeometryPosition value is "Outside".  **Example:**     The following example gets the Start point geometry on the Pocketing operation Pocketing1

```VBScript
     Call Pocketing1.GetStartPointGeometry(Position,Point1,Part,OffsetValue)

```

### Sub **GetToolGage**( double  `oMinToolLength`,  double  `oMinToolGage`)

   Retrieves the minimum tool cutting lentgh and the minimum tool gage length.

**Example:**     The following example Retrieves in `MinToolLength` and `MinToolGage` the values of tool of Manufacturing Operation `Operation`

```VBScript
     Call Operation.GetToolGage(MinToolLength,MinToolGage)

```

### Sub **GetTrajectoryEndPointCoord**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oEndPoint`)

   Retrieve the Machining Operation's trajectory end point.

**Example:**     The following example Retrieves in `oEndPoint` the end point of the Machining Operation `Operation`

```VBScript
     Dim oEndPoint(2)
     call Operation.GetTrajectoryEndPointCoord(oEndPoint)
     x = oEndPoint(0)
     y = oEndPoint(1)
     z = oEndPoint(2)

```

### Sub **GetTrajectoryStartPointCoord**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oStartPoint`)

   Retrieve the Machining Operation's trajectory start point.

**Example:**     The following example Retrieves in `oStartPoint` the start point of the Machining Operation `Operation`

```VBScript
     Dim oEndPoint(2)
     call Operation.GetTrajectoryStartPointCoord(oStartPoint)
     x = oStartPoint(0)
     y = oStartPoint(1)
     z = oStartPoint(2)

```

### Func **InsertToolMotion**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  short  `iPosition`) As [CATIAManufacturingToolMotion](../ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)

   Create, given its type, a Manufacturing ToolMotion inside a sequential operation.

    The available type for lathe sequential operation are :     for GoStandard and GoGo tool motion iType = `MfgSeqMotionLatheGoStd`     for GoDelta tool motion, iType = `MfgSeqMotionLatheDelta`     for Indirv tool motion, iType = `MfgSeqMotionLatheIndirv`     for Follow tool motion, iType = `MfgSeqMotionLatheFollow`     for PPWord tool motion, iType = `MfgSeqMotionPPWord`          The available type for prismatic sequential operation are :     for Goto Point tool motion, iType = `MfgSeqMotionPoint`     for Goto Position tool motion, iType = `MfgSeqMotionPosition`     for Goto Delta tool motion, iType = `MfgSeqMotionDelta`      `iType` type of the ToolMotion to be created `iPosition` rank in the operation list where the ToolMotion will be created      iPosition=0 means creation at the end of the list of tool motions `oToolMotion` the created ManufacturingToolMotion          The following example creates in ManufacturingOperation `SeqMO`      which is a Lathe Sequential operation     the ManufacturingToolMotion `ThisToolMotion` of type `MfgSeqMotionLatheGoStd` at the first rank

```VBScript

     **Example:**
    	Set SeqMO = Program1.AppendOperation("MfgLatheMfgSequentialOperation",1)
    	Set ThisToolMotion = SeqMO.InsertToolMotion("MfgSeqMotionLatheGoStd",1)

```

    The following example creates in ManufacturingOperation `SeqMO`      which is an Axial Point to Point sequential operation     the ManufacturingToolMotion `ThisToolMotion` of type `MfgSeqMotionPoint` at the first rank

```VBScript

     **Example:**
    	Set SeqMO = Program1.AppendOperation("PointToPoint",1)
    	Set ThisToolMotion = SeqMO.InsertToolMotion("MfgSeqMotionPoint",1)

```

### Func **IsGeometricallyAccessibleOnSetup**( [CATIABase](../System/interface_AnyObject_17321.md)  `iManufacturingSetup`) As boolean

   Returns True if the Manufacturing Axial Operation is geometrically accessible on the given Manufacturing Setup.The Axial Operation must have a valid tool axis and a machine must be assigned to the Manufacturing Setup. If this is not the case, the method returns False.

**Parameters:**

` iSetup`      The Manufacturing Setup gives the accessibility checking context : the part,the machine and the relative orientation of the part on the machine.

**Example:**     The following example checks the accessibility of `firstOperation` on `firstSetup`.

```VBScript
     Dim isAccessible As Boolean
     isAccessible = firstOperation.IsGeometricallyAccessibleOnSetup(firstSetup)

```

### Sub **RemoveRelimitingGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`)

   Removes the geometry on relimiting element PROFILE CONTOURING operation ONLY.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be:

`"StartElement"`, to remove the Start element on Profile Contouring      `"EndElement"`, to remove the End element on Profile Contouring      **Example:**     The following example removes the End relimiting element of the Profile Contouring operation Contouring1

```VBScript
     Call Contouring1.RemoveRelimitingGeometry("EndElement")

```

### Sub **RemoveStartPointGeometry**( )

   Removes the start point element on POCKETING operation ONLY.

**Example:**     The following example removes the start point of the Pocketing operation Pocketing1

```VBScript
     Call Pocketing1.RemoveStartPointGeometry

```

### Sub **SetFeature**( [CATIABase](../System/interface_AnyObject_17321.md)  `iMachinableFeature`)

   Associate a Machinable Feature to a Manufacturing Operation.

**Example:**     The following example associates in `firstOperation` the machinable feature `Feature`

```VBScript
     call firstOperation.SetFeature(Feature)

```

### Sub **SetFeedSpeedAutoUpdate**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  boolean  `iAutoUpdate`)

   Set the Auto Update status for Feed Rate or Spindle Speed.

**Parameters:**

` iType`      Determines if the method works on Feed Rate or Spindle Speed **Legal values** : iType can be

  * `"FEEDRATE"`
  * `"SPINDLESPEED"`

` iAutoUpdate`      Auto update status **Legal values** : iType can be

  * `True`
  * `False`

    * **Example:**
    * The following example enables AutoUpdate for Spindle Speed
    * firstOperation.SetFeedSpeedAutoUpdate("SPINDLESPEED", True)

### Sub **SetFeedrateMagnitude**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`)

   Defines the magnitude of the feedrate values.

```VBScript

         The available types for Magnitude are:
         for Linear Magnitude , iMagnitudeName = LINEARFEEDRATE
         for Angular Magnitude , iMagnitudeName = ANGULARFEEDRATE

     **Example:**
     Dim Operation1 As ManufacturingOperation
     Set Operation1 = Program1.AppendOperation ("Drilling",1)
     Operation1.SetFeedrateMagnitude("LINEARFEEDRATE")

```

### Sub **SetGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  short  `iPosition`)

   Assigns geometry to a Manufacturing Operation.

**Parameters:**

` iGeometryType`      Type of geometry to assign (Parts, Drives, ..)
` iReference`      Geometry to assign: it may be a feature (point, hole, ..) or a BREP feature.
` iProduct`      Product containing the geometry to assign. It must be the occurence of the product which owns the part containing the geometry. Also see method GetProductInstance of CATIAManufacturingSetup interface.
` iPosition`      Position of the geometry in the list (0 to append at the end of the list). **Example:**     The following example assigns the plane `Plane.1` as bottom of operation ` Pocketing1 ` of the Manufacturing Program `Program1`. The Product `Product1` is associated to Manufacturing Setup ` Setup1`. This example is valid only if the Product owning the part which contains the plane has been associated to the Manufacturing Setup (if the CATPart containing the plane has been associated to the Manufacturing Setup). In other cases, the product must be retrieved differently.

```VBScript
     Set Product1 = Setup1.GetProductInstance()
     Dim Pocketing1 As ManufacturingOperation
     Set Pocketing1 = Program1.AppendOperation ("Pocketing",1)
     Pocketing1 .SetGeometry("PartBottom",Plane1,Product1,0)

```

### Sub **SetPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPattern`)

   Associate a Machining Pattern to a Manufacturing Operation.

**Example:**     The following example associates in `firstOperation` the machining pattern `Pattern`

```VBScript
     call firstOperation.SetPattern(Pattern)

```

### Sub **SetRadiusOnMacro**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMacroType`,  double  `iRadius`)

   Defines radius attribute on the circular elementary macro motion on CIRCULAR MILLING or THREAD MILLING operations ONLY.

**Parameters:**

` iMacroType`      **Legal values** : iMacroType can be:

`"Approach"`, to set the radius on the Approach Macro      `"Retract"`, to set the radius on the Retract Macro      `"ReturnInALevelApproach"`, to set the radius on the Return in a level Macro (Approach)      `"ReturnInALevelRetract"`, to set the radius on the Return in a level Macro (Retract)      `"ReturnBetweenLevelsApproach"`, to set the radius on the Return between levels Macro (Approach)      `"ReturnBetweenLevelsRetract"`, to set the radius on the Return between levels Macro (Approach)
` iRadius`      Radius value. (expressed in millimeters)  **Example:**     The following example sets a radius 5mm on the circular motion of the retract macro on the Circular Milling operation CircularMilling1

```VBScript
     Dim CircularMilling1 As ManufacturingOperation
     Set CircularMilling1 = Program1.AppendOperation ("CircularMilling1",1)
     Call CircularMilling1.SetRadiusOnMacro("Retract",5.00)

```

### Sub **SetRelimitingGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  double  `iOffset`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPosition`)

   Defines start / end element on PROFILE CONTOURING operation ONLY.
Sets a geometry on relimiting element in profile contouring operation.

**Parameters:**

` iGeometryType`      **Legal values** : iGeometryType can be:

`"StartElement"`, to set the Start element on Profile Contouring      `"EndElement"`, to set the End element on Profile Contouring
` iReference`      Geometries to be set. It can be a list of curves or a single point. The curves must be adjacent.
` iProduct`      Product containing the geometry to be set.
` iOffset`      Offset to set on the relimiting geometry. (expressed in millimeters)
` iPosition`      Tool position to set on the relimiting geometry.

**Legal values** : iPosition can be:

`"IN"`, to set the tool position IN      `"ON"`, to set the tool position ON      `"OUT"`, to set the tool position OUT      **Example:**     The following example sets the Start relimiting element Curve1 on the Profile Contouring operation Contouring1

```VBScript
     Call Contouring1.SetRelimitingGeometry("StartElement",Curve1,PartMachined,3.00,"ON")

```

### Sub **SetSpindleMagnitude**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`)

   Defines the magnitude of the spindle values.

```VBScript

         The available types for Magnitude are:
         for Linear Magnitude , iMagnitudeName = LINEARSPINDLESPEED
         for Angular Magnitude , iMagnitudeName = ANGULARSPINDLESPEED

     **Example:**
     Dim Operation1 As ManufacturingOperation
     Set Operation1 = Program1.AppendOperation ("Drilling",1)
     Operation1.SetSpindleMagnitude("ANGULARSPINDLESPEED")

```

### Sub **SetStartPointGeometry**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGeometryPosition`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iProduct`,  double  `iOffset`)

   Defines the geometry and the offset of a start point on POCKETING operation ONLY.

**Parameters:**

` iGeometryPosition`      **Legal values** : iGeometryPosition can be:

`"Outside"`, to set the Start point outside the pocket contour      `"Inside"`, to set the Start point inside the pocket contour
` iReference`      Geometry to be set. It can be a point.
` iProduct`      Product containing the geometry to be set.
` iOffset`      Offset set on the start point. (expressed in millimeters)
Offset is taken into account only if iGeometryPosition is set to "Outside".  **Example:**     The following example sets Point1 as Start point on the Pocketing operation Pocketing1

```VBScript
     Call Pocketing1.SetStartPointGeometry("Inside",Point1,PartMachined,0.00)

```

### Sub **SetTool**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolName`)

   Assign an already created tool to a Manufacturing Operation.
If the tool is not already created, or if it is not authorized for this kind of Manufacturing Operation, a default tool is created.

**Example:**     The following example assign a drill tool named `D-9.7` on the operation ` MO1` of the Manufacturing Program `Program1` A tool change with tool `D-9.7` has already been created in the Manufacturing Program.

```VBScript
     Dim Operation1 As ManufacturingOperation
     Set Operation1 = Program1.AppendOperation ("Drilling",1)
     Operation1.SetTool("D-9.7")

```

---

# ManufacturingOutput (Object)

**_Object that represents the output machining code._**

## Properties

### Property **Size**( ) As long (Read Only)

   Returns the number of bytes written to this data output.

**Parameters:**

` oBytes`      The integer value of the number of bytes
Methods

### Sub **CloseStream**( )

   Close the Stream.  
### Sub **DecrementTabulation**( long  `iTab`)

   Decrement the tabulation of the current block of text by the specified number of characters.  
### Sub **EndBlock**( )

   Specify that the Block is ended.  
### Sub **EndLine**( )

   Specify that the line is ended.  
### Sub **Flush**( )

   Flush all Data in the Stream.  
### Sub **IncrementTabulation**( long  `iTab`)

   Increment the tabulation of the current block of text by the specified number of characters.  
### Sub **NewBlock**( )

   Create a New Block in the underlying output stream.  
### Sub **NewLine**( )

   Create a New Line in the underlying output stream.  
### Sub **SetBufferLength**( long  `iLines`)

   Set the number of lines of the buffer before it will be flushed (default is 200).

**Parameters:**

` iLines`      The integer value of the number of lines

### Sub **write_Chars**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iText`)

   Write the specified string to the underlying output stream.  
### Sub **write_Double**( double  `iVal`)

   Write the specified double to the underlying output stream.  
### Sub **write_Long**( long  `iVal`)

   Write the specified long to the underlying output stream.

---

# ManufacturingOutputGenerator (Object)

**_Father object to generate output machining code._**

## Methods

### Sub **AddMeToBuffer**( long  `oAddMe`)

   Management of specific buffer for aligned points elimination.  
### Sub **GenerateOutputCode**( [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `iData`)

   Return the Output Code for an object in the right CNC Machine.  
### Sub **GetAPTCode**( [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `iData`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oCode`)

   Retrieve generated APT code.  
### Sub **GetCurrentObject**( long  `oCurrentObject`)

   Get current object from buffer.  
### Sub **HasToResetModalValues**( long  `oIsModal`)

   Return the characteristic of an object : Reset or not Modal Values.  
### Sub **InitFileGenerator**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFormat`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `oData`)

   Init the Output Generator on the current Object and initialise all datas. Generation of NC code can start from the Process, Setup, Program or an Activity.

**Parameters:**

` iFormat`      Format of the output file : "APT", ...
` iFileName`      Output file name
` oData`      iData contains all the information about the generated NC code

### Sub **IsModal**( long  `oIsModal`)

   Return the characteristic of an object : Modal or Not Modal.  
### Func **IsSimilarTo**( [CATIAManufacturingOutputGenerator](../ManufacturingInterfaces/interface_ManufacturingOutputGenerator_169508.md)  `iObject`) As long

   Implement a method to specify if two objects are same (when Modal Mode). The result depends on the tolerance on the values (to points)  
### Sub **RunFileGenerator**( [CATIAManufacturingGeneratorData](../ManufacturingInterfaces/interface_ManufacturingGeneratorData_141888.md)  `iData`)

   Runs the Output Generator on the datas used for generation. Generation of NC code can start from the Process, Setup, Program or an Activity.

**Parameters:**

` iData`      iData contains all the information about the generated NC code

### Sub **SetCurrentObject**( long  `iCurrentObject`)

   Set current object to buffer.

---

# ManufacturingPattern (Object)

**_The Manufacturing Pattern is a specialized feature used to machine the same item several times at several positions._**

## Properties

### Property **ToolAxisStrategy**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Tool Axis Strategy of a Manufacturing Pattern.

**Legal values** : The parameter name can be

`Fixed`      `Variable`      `NormalToPS`      **Examples:**     The following example returns the Tool Axis Strategy `ThisToolAxisStrategy` of the manufacturing pattern `CurrentMfgPattern`

```VBScript
     Dim ThisToolAxisStrategy As CATBSTR
     ThisToolAxisStrategy = CurrentMfgPattern.ToolAxisStrategy

```

The next example sets the Tool Axis Strategy of the manufacturing pattern `CurrentMfgPattern`

```VBScript
     CurrentMfgPattern.ToolAxisStrategy = "Fixed"

```

Methods

### Sub **ActivatePoint**( short  `iPointNumber`)

   Activates a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point to activate.

**Example:**     The following example activates the point number 2 of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.ActivatePoint(2)

```

### Sub **AddPartSurface**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPartSurface`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  short  `iNotify`)

   Adds a Part Surface to the Manufacturing Pattern.

**Parameters:**

` iPartSurface`      The part surface to be added.
` iProduct`      The product containing the part surface to add.
` iNotify`      The flag to specify if a refresh of the visualization is needed. Usually, this parameter is set to 1. In the case of a loop, it should be set to 1 only on the last call of the method.

**Legal values** : The parameter can be

`0`      no notification is sent `1`      a notification is sent

**Example:**     The following example adds the part surface 'TopPlane' to the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.AddPartSurface(TopPlane,Product1,1)

```

### Sub **AddPosition**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPosition`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  short  `iNotify`)

   Adds a position to the Manufacturing Pattern.

**Parameters:**

` iPosition`      The position to be added.

**Legal values** : The position can be a

`Design Hole`      the point is the origin point of the hole `Design Pattern`      points are retrieved from the design pattern `Point`      the point coordinates are retrieved from the added point `Circle`      the point is the center of the circle
` iProduct`      The product containing the position to add.
` iNotify`      The flag to specify if a refresh of the visualization is needed. Usually, this parameter is set to 1. In the case of a loop, it should be set to 1 only on the last call of the method.

**Legal values** : The parameter can be

`0`      no notification is sent `1`      a notification is sent

**Example:**     The following example adds the position 'DesignPattern1' to the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.AddPosition(DesignPattern1,Product1,1)

```

### Sub **DeactivatePoint**( short  `iPointNumber`)

   Deactivates a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point to deactivate.

**Example:**     The following example deactivates the point number 2 of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.DeactivatePoint(2)

```

### Func **GetAnAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retreive the attribute of Manufacturing Pattern from its name.

**Parameters:**

` iAttribute`      The identifier of the attribute to be read.

**Legal values** : The identifier can be

`JumpDistance`      the jump distance of the pattern `TopMode`      the Top Mode of the pattern

**Example:**     The following example retrieves the attribute 'JumpDistance' of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.GetAnAttribute(JumpDistance,JumpParm)

```

### Sub **GetLocalToolAxis**( short  `iPointNumber`,  double  `oX`,  double  `oY`,  double  `oZ`)

   Retrieve the local tool axis of a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point on which the tool axis is set.
` oX`      The first coordinate of the tool axis.
` oY`      The second coordinate of the tool axis.
` oZ`      The third coordinate of the tool axis.

**Example:**     The following example retrieves the tool axis of the point number 3 of manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.GetLocalToolAxis(3,oX,oY,oZ)

```

### Sub **GetNumbers**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oNumbers`)

   Retrieve the number of the points of a Manufacturing Pattern.

**Parameters:**

` oNumbers`      The numbers of the points of the pattern.

**Example:**     The following example retrieves the numbers of the points of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.GetNumbers(oNumbers)

```

### Sub **RemovePartSurfaces**( )

   Remove the Part Surfaces of the Manufacturing Pattern.

**Example:**     The following example removes the part surfaces of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.RemovePartSurfaces()

```

### Sub **Reverse**( )

   Reverses the numbering of a Manufacturing Pattern.

**Example:**     The following example reverses the numbering of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.Reverse()

```

### Sub **SetItemToCopy**( [CATIABase](../System/interface_AnyObject_17321.md)  `iItem`)

   Sets the feature to be copied.

**Parameters:**

` iItemToCopy`      The feature to be copied. It may be a Design Hole or a Manufacturing Hole.

**Legal values** : The parameter name can be

`Diameter`     The hole diameter
` oParameter`      The value of the parameter

**Example:**     The following example sets the item to copy 'Hole1' to the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.SetItemToCopy(Hole1)

```

### Sub **SetLocalToolAxis**( short  `iPointNumber`,  double  `iX`,  double  `iY`,  double  `iZ`)

   Sets a local tool axis to a point of a Manufacturing Pattern.

**Parameters:**

` iPointNumber`      The number of the point on which the tool axis is set .
` iX`      The first coordinate of the tool axis.
` iY`      The second coordinate of the tool axis.
` iZ`      The third coordinate of the tool axis.

**Example:**     The following example sets the Z axis as tool axis of the point number 3 of manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.SetLocalToolAxis(3,0,0,1)

```

### Sub **StartPoint**( short  `iPointNumber`)

   Sets a point of a Manufacturing Pattern as the start point.

**Parameters:**

` iPointNumber`      The number of the point to set as start point.

**Example:**     The following example sets the point number 2 as the start point of the manufacturing pattern `mfgPattern`:

```VBScript
     call mfgPattern.StartPoint(2)

```

---

# ManufacturingPrecedence (Object)

**_Defines a precedence relation between objects._**

## Properties

### Property **PrecedenceType**( ) As [CatManufacturingPrecedenceType](../ManufacturingInterfaces/enum_CatManufacturingPrecedenceType_188280.md) (Read Only)

   Returns the type of the precedence.  
### Property **TargetOperation**( ) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md) (Read Only)

   Returns the target object of the precedence, but with the Operation interface if it is.

---

# ManufacturingPrecedences (Collection)

**_Interface that manage the precedences for an object of type @ CATIAManufacturingActivity._**
If an object A has objects B and C as precedence constraints, it means that B and C have to be performed before A.

## Methods

### Sub **AddOperation**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iObject`,  [CatManufacturingPrecedenceType](../ManufacturingInterfaces/enum_CatManufacturingPrecedenceType_188280.md)  `iType`)

   Adds a new precedence in the collection of precedences. The type of added object is a CATIAManufacturingActivity.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAManufacturingPrecedence](../ManufacturingInterfaces/interface_ManufacturingPrecedence_111444.md)

   Returns a precedence object from the precedence collection.  
### Sub **Remove**( long  `iIndex`)

   Removes an object from the precedences collection. The removed precedence will be deleted, but not the referenced object attach to this precedence.  
### Sub **RemoveAll**( )

   Removes all objects from the precedences collection.

---

# ManufacturingProcess (Object)

**_A ManufacturingProcess for a Manufacturing Document._**

## Properties

### Property **Setups**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md) (Read Only)

   Give the List of Setups linked to a Manufacturing Process.

**Example:**     The following example returns the list of Setups `SetupsList` linked to the manufacturing Process `CurrentProcess`

```VBScript
     Set SetupsList = CurrentProcess.Setups

```

---

# ManufacturingProgram (Object)

**_A ManufacturingProgram for a Manufacturing Document._**

## Properties

### Property **Activities**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md) (Read Only)

   Give the List of Activities linked to a Manufacturing Program.

**Example:**     The following example returns the list of Activities `ActivitiesList` linked to the manufacturing Program `CurrentProgram`

```VBScript
     Set ActivitiesList = CurrentProgram.Activities

```

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Return the Default Comment of a Manufacturing Program.

**Example:**     The following example return the comment `ProgramComment` of to the manufacturing Program `CurrentProgram`

```VBScript
     Set CurrentProgram.Comment= "ProgramComment"

```

Methods

### Func **AddGotoPoint**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPointName`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   Add a Goto Point Operation to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a PTP point instruction GOTO1 to the Point wich alias is`MyPoint`

```VBScript
     Set GOTO1 = firstProgram.AddGotoPoint(MyPoint)

```

### Func **AddGotoPointfromCoordinates**( double  `iX`,  double  `iY`,  double  `iZ`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   Add a Goto Point Operation to a Manufacturing Program.

```VBScript
     The coordinates you give as input for this method have to be expressed into
     the 'Absolute Axis System' not in the 'Machining Axis System' of the Part Operation.

```

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a PTP point instruction GOTO1 to the Point wich coordinates are`X,Y,Z`

```VBScript
     Set GOTO1 = firstProgram.AddGotoPointfromCoordinates(X,Y,Z)

```

### Func **AddPPInstruction**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPPInstruction`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   Add a PP Instruction to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a PP Instruction PPWORD1 with text`PPWORD`

```VBScript
     Set PPWORD1 = firstProgram.AddPPInstruction(PPWORD)

```

### Func **AddRotabl**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRotabl`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSens`,  double  `ival`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   Add a Table Head Rotation instruction to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a Rotabl ROTABL1 with argument`MODE` and angle`ANGLE1`

```VBScript
     Set ROTABL1 = firstProgram.AddRotabl(MODE,ANGLE1)

```

### Func **AddToolChange**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolCatalog`,  short  `iNumSyntaxe`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   Add a Tool Change Operation to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in `firstProgram` a Tool Change Instruction with specified tool`MyTool` of specified type `ToolType`in specified catalog`ToolCatalog`

```VBScript
     Set ToolChange1 = firstProgram.AddToolChange(MyTool,ToolType,ToolCatalog,Num)

```

### Func **AddToolChangeMultipleFeeds**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolCatalog`,  short  `iNumFSData`,  short  `iNumSyntaxe`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   Add a Tool Change Operation to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in `firstProgram` a Tool Change Instruction with specified tool`MyTool` of specified type `ToolType`in specified catalog`ToolCatalog`

```VBScript
     Set ToolChange1 = firstProgram.AddToolChangeMultipleFeeds(MyTool,ToolType,ToolCatalog,NumFSData,Num)

```

### Func **AppendOperation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `type`,  short  `AutoSequence`) As [CATIAManufacturingOperation](../ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)

   Create and Insert a Manufacturing Operation of a specified type to a Manufacturing Program.
if AutoSequence is set to 1, the new operation will be sequenced in the Program.

**Example:**     The following example creates, inserts and sequences in `firstProgram` the manufacturing operation `ManufacturingOperation` of type : `type`

```VBScript
     Set ManufacturingOperation = firstProgram.AppendOperation(Type,1)

```

### Sub **CompletewithPolarStrategy**( [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)  `iListeMfgActivity`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAxeRef`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSensRotation`)

   Complete a list of Operation in a Manufacturing Program in Polar Mode.

**Example:**     The following example complete in Program `firstProgram` a liste of Operation `ListeMo` with Reference Axis `A` and sens `CLW`

```VBScript
     Call firstProgram.CompletewithPolarStrategy(ListeMo,A,CLW)

```

### Func **CreateMOfromReport**( [CATIAExpertReportObjects](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md)  `iReportSucceed`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMo`) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)

   Create a list of Operation in a Manufacturing Program, of a specified type.

**Example:**     The following example create in Program `firstProgram` a liste of Operation `ListeMo` with type `Drilling` from a CATIAExpertReportSucceedCollection `ReportSucceed`.

```VBScript
     Set ListeMO = firstProgram.CreateMOfromReport(ReportSucceed,Drilling)

```

### Func **GetNCOutputFile**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Get the output file (APT or ISO) associated to the program (if associated during computation).

### Func **GetTableCurrentAbsolutePosition**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iActivityRef`) As double

   Get the current absolute position of the Machine Table.

**Example:**     The following example gets in Program `firstProgram` the current Machine Table absolute position `Angle` from the Manufacturing activity reference `iActivityRef`

```VBScript
     Angle = firstProgram.GetTableCurrentAbsolutePosition(iActivityRef)

```

### Sub **InsertOperation**( [CATIAManufacturingOperation](../ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)  `iReferenceOperation`,  [CATIAManufacturingOperation](../ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)  `iManufacturingOperation`)

   Insert an existing Manufacturing Operation to a Manufacturing Program.

**Example:**     The following example inserts in `firstProgram` the manufacturing operation `ExistingOperation` after `ReferenceOperation`:

```VBScript
     call firstProgram.InsertOperation(ReferenceOperation,ExistingOperation)

```

### Sub **MoveOperation**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iReferenceOperation`,  [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iManufacturingOperation`)

   Move an existing Manufacturing Operation to a Manufacturing Program.

**Example:**     The following example moves in `firstProgram` the manufacturing operation `MovedOperation` after the manufacturing operation`ExistingOperation`:

```VBScript
     call firstProgram.MoveOperation(ExistingOperation, MovedOperation)

```

### Func **OrderAndCreateMOfromReport**( [CATIAExpertReportObjects](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md)  `iReportSucceed`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMo`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAxeRotabl`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSensRotation`) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)

   Create a list of Operation in a Manufacturing Program, of a specified type.

**Example:**     The following example create in Program `firstProgram` a liste of Operation `ListeMo` with type `Drilling` from a CATIAExpertReportSucceedCollection `ReportSucceed` with Rotabl of Axis `A` and sens `CLW`.

```VBScript
     Set ListeMO = firstProgram.OrderAndCreateMOfromReport(ReportSucceed,Drilling)

```

---

# ManufacturingSetup (Object)

**_A ManufacturingSetup for a Manufacturing Document._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Return the Default Comment of a Manufacturing Setup.

**Example:**     The following example return the comment `SetupComment` of to the manufacturing setup `CurrentSetup`

```VBScript
     Set CurrentSetup.Comment= "SetupComment"

```

### Property **Machine**( ) As [CATIAManufacturingMachine](../ManufacturingInterfaces/interface_ManufacturingMachine_84488.md)

   Give the Machine linked to a Manufacturing Setup.

**Example:**     The following example returns the `Machine` linked to the manufacturing setup `CurrentSetup`

```VBScript
     Set Machine = CurrentSetup.Machine

```

### Property **MachiningAxisSystem**( ) As [CATIAManufacturingMachiningAxis](../ManufacturingInterfaces/interface_ManufacturingMachiningAxis_142294.md)

   Retrieves the Machining Axis system from a Manufacturing Setup.

**Example:**     The following example retrieves the Machining Axis system `oMachiningAxis` from the manufacturing setup `CurrentSetup`

```VBScript
     Set oMachiningAxis = CurrentSetup.MachiningAxisSystem

```

### Property **Product**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Associate the Product to a Manufacturing Setup.

**Example:**     The following example associates the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
     CurrentSetup.Product = iProduct

```

### Property **Programs**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md) (Read Only)

   Give the List of Programs linked to a Manufacturing Setup.

**Example:**     The following example returns the list of Programs `ProgramsList` linked to the manufacturing Setup `CurrentSetup`

```VBScript
     Set ProgramsList = CurrentSetup.Programs

```

Methods

### Func **CreateMachine**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMachine`) As [CATIAManufacturingMachine](../ManufacturingInterfaces/interface_ManufacturingMachine_84488.md)

   Initialise the Manufacturing Machine linked to a Manufacturing Setup.

**Example:**     The following example initialise the machine `Mfg3AxisWithTableRotationMachine` as Manufacturing Machine in the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.CreateMachine(Mfg3AxisWithTableRotationMachine)

```

### Func **DesignGeometriesCount**( ) As long

   Returns the number of design geometries from a Manufacturing Setup.

**Parameters:**

` oDesignGeometriesListSize`      The number of design geometries of this setup  **Example:**     The following example retrieves the number of design geometries of the setup `CurrentSetup` in `DesignGeometriesListSize`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim DesignGeometriesListSize As Long
     DesignGeometriesListSize = CurrentSetup.DesignGeometriesCount

```

### Func **FixtureGeometriesCount**( ) As long

   Returns the number of fixture geometries from a Manufacturing Setup.

**Parameters:**

` oFixtureGeometriesListSize`      The number of fixture geometries of this setup  **Example:**     The following example retrieves the number of fixture geometries of the setup `CurrentSetup` in `FixtureGeometriesListSize`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim FixtureGeometriesListSize As Long
     FixtureGeometriesListSize = CurrentSetup.FixtureGeometriesCount

```

### Func **GetMachiningAxisSystemName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the Name of the Machining Axis system from a Manufacturing Setup.

**Example:**     The following example retrieves the Name of the Machining Axis system`oMachiningAxisSystemName` from the manufacturing setup `CurrentSetup`

```VBScript
     Set oMachiningAxisSystemName = CurrentSetup.GetMachiningAxisSystemName

```

### Func **GetManufacturingView**( ) As [CATIAManufacturingView](../ManufacturingInterfaces/interface_ManufacturingView_62589.md)

   Retrieves the Manufacturing View from a Manufacturing Setup.

**Example:**     The following example retrievec the Manufacturing View `MfgView` from the manufacturing setup `CurrentSetup`

```VBScript
     Set MfgView = CurrentSetup.GetManufacturingView

```

### Func **GetPartName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the Name of the Design Part from a Manufacturing Setup.

**Example:**     The following example retrieves the Name of the Design Part`oPartName` from the manufacturing setup `CurrentSetup`

```VBScript
     Set oPartName = CurrentSetup.GetPartName

```

### Func **GetProductInstance**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Give the Product of the ProductList linked to a Manufacturing Setup.

**Example:**     The following example returns the `Product` linked to the manufacturing setup `CurrentSetup`

```VBScript
     Set Product = CurrentSetup.GetProductInstance

```

### Func **GetSafetyPlane**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retrieves the Safety Plane from a Manufacturing Setup.

**Example:**     The following example retrieves the Safety Plane `oMathPLane` from the manufacturing setup `CurrentSetup` The size of oMathPlane is 9 (origin, first direction, second direction)

```VBScript
     Set oMathPlane= CurrentSetup.GetSafetyPlane

```

### Sub **GetStockFromSetup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oStockPath`)

   Retrieves the path of the Stock file from a Manufacturing Setup.

**Example:**     The following example retrieves the the path of the Stock file`oStockPath` from the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.GetStockFromSetup(oStockPath)

```

### Sub **GetToolChangePoint**( double  `oX`,  double  `oY`,  double  `oZ`)

   Get the ToolChange point of the machine linked to a Manufacturing Setup.

**Example:**     The following example gets the point with coordinates `X,Y,Z` as ToolChangePoint in the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.GetToolChangePoint(X,Y,Z)

```

### Func **InProcessModelBodiesCount**( ) As long

   Returns the number of In Process Model Bodies from a Manufacturing Setup.

**Parameters:**

` oIPMBodiesListSize`      The number of In Process Model Bodies of this setup  **Example:**     The following example retrieves the number of In Process Model Bodies of the setup `CurrentSetup` in `IPMBodiesListSize`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim IPMBodiesListSize As Long
     IPMBodiesListSize = CurrentSetup.InProcessModelBodiesCount

```

### Sub **ListDesignGeometries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfDesignGeometries`)

   Retrieves the design geometries list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfDesignGeometries`      The retrieved list.
The array must be previously initialized using the
DesignGeometriesCount method.  **Example:**     The following example retrieves the design geometries list of the manufacturing setup `CurrentSetup` in `ListOfDesignGeometries`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim DesignGeometriesListSize As Long
     DesignGeometriesListSize = CurrentSetup.DesignGeometriesCount
     If DesignGeometriesListSize > 0 Then
       Dim ListOfDesignGeometries() As Variant
       Redim ListOfDesignGeometries(DesignGeometriesListSize-1)
       CurrentSetup.ListDesignGeometries(ListOfDesignGeometries)
     End If

```

### Sub **ListDesignGeometriesProducts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfDesignGeometriesProducts`)

   Retrieves the design geometries products list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfDesignGeometriesProducts`      The retrieved list.
The array must be previously initialized using the
DesignGeometriesCount method.  **Example:**     The following example retrieves the design geometries list of the manufacturing setup `CurrentSetup` in `ListOfDesignGeometriesProducts`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim DesignGeometriesListSize As Long
     DesignGeometriesListSize = CurrentSetup.DesignGeometriesCount
     If DesignGeometriesListSize > 0 Then
       Dim ListOfDesignGeometries() As Variant
       Redim ListOfDesignGeometries(DesignGeometriesListSize-1)
       CurrentSetup.ListDesignGeometriesProducts(ListOfDesignGeometriesProducts)
     End If

```

### Sub **ListFixtureGeometries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfFixtureGeometries`)

   Retrieves the fixture geometries list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfFixtureGeometries`      The retrieved list.
The array must be previously initialized using the
FixtureGeometriesCount method.  **Example:**     The following example retrieves the fixture geometries list of the manufacturing setup `CurrentSetup` in `ListOfFixtureGeometries`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim FixtureGeometriesListSize As Long
     FixtureGeometriesListSize = CurrentSetup.FixtureGeometriesCount
     If FixtureGeometriesListSize > 0 Then
       Dim ListOfFixtureGeometries() As Variant
       Redim ListOfFixtureGeometries(FixtureGeometriesListSize-1)
       CurrentSetup.ListFixtureGeometries(ListOfFixtureGeometries)
     End If

```

### Sub **ListFixtureGeometriesProducts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfFixtureGeometriesProducts`)

   Retrieves the Fixture geometries products list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfFixtureGeometriesProducts`      The retrieved list.
The array must be previously initialized using the
FixtureGeometriesCount method.  **Example:**     The following example retrieves the Fixture geometries list of the manufacturing setup `CurrentSetup` in `ListOfFixtureGeometriesProducts`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim FixtureGeometriesListSize As Long
     FixtureGeometriesListSize = CurrentSetup.FixtureGeometriesCount
     If FixtureGeometriesListSize > 0 Then
       Dim ListOfFixtureGeometries() As Variant
       Redim ListOfFixtureGeometries(FixtureGeometriesListSize-1)
       CurrentSetup.ListFixtureGeometriesProducts(ListOfFixtureGeometriesProducts)
     End If

```

### Sub **ListInProcessModelBodies**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfIPMBodies`)

   Retrieves the In Process Model Bodies list from a Manufacturing Setup.

**Parameters:**

` oListOfIPMBodies`      The retrieved list.
The array must be previously initialized using the
InProcessModelBodiesCount method.  **Example:**     The following example retrieves the In Process Model Bodies list of the manufacturing setup `CurrentSetup` in `ListOfIPMBodies`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim IPMBodiesListSize As Long
     IPMBodiesListSize = CurrentSetup.InProcessModelBodiesCount
     If IPMBodiesListSize > 0 Then
       Dim ListOfIPMBodies() As Variant
       Redim ListOfIPMBodies(IPMBodiesListSize-1)
       CurrentSetup.ListInProcessModelBodies(ListOfIPMBodies)
     End If

```

### Sub **ListStockGeometries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfStockGeometries`)

   Retrieves the stock geometries list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfStockGeometries`      The retrieved list.
The array must be previously initialized using the
StockGeometriesCount method.  **Example:**     The following example retrieves the stock geometries list of the manufacturing setup `CurrentSetup` in `ListOfStockGeometries`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim StockGeometriesListSize As Long
     StockGeometriesListSize = CurrentSetup.StockGeometriesCount
     If StockGeometriesListSize > 0 Then
       Dim ListOfStockGeometries() As Variant
       Redim ListOfStockGeometries(StockGeometriesListSize-1)
       CurrentSetup.ListStockGeometries(ListOfStockGeometries)
     End If

```

### Sub **ListStockGeometriesProducts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfStockGeometriesProducts`)

   Retrieves the Stock geometries products list from a Manufacturing Setup. Each of these geometries may be either a Product or a Body.

**Parameters:**

` oListOfStockGeometriesProducts`      The retrieved list.
The array must be previously initialized using the
StockGeometriesCount method.  **Example:**     The following example retrieves the Stock geometries list of the manufacturing setup `CurrentSetup` in `ListOfStockGeometriesProducts`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim StockGeometriesListSize As Long
     StockGeometriesListSize = CurrentSetup.StockGeometriesCount
     If StockGeometriesListSize > 0 Then
       Dim ListOfStockGeometries() As Variant
       Redim ListOfStockGeometries(StockGeometriesListSize-1)
       CurrentSetup.ListStockGeometriesProducts(ListOfStockGeometriesProducts)
     End If

```

### Sub **SetProductAndReconciliate**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Associate the Product to a Manufacturing Setup and reconciliate links.

**Example:**     The following example associates the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.SetProductAndReconciliate(iProduct)

```

### Sub **SetSafetyPlane**( [CATIABase](../System/interface_AnyObject_17321.md)  `iSafetyPlane`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Associates a Safety Plane to a Manufacturing Setup.

**Example:**     The following example associates the Safety Plane `iSafetyPlane` belonging to the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.SetSafetyPlane(iSafetyPlane,iProduct)

```

### Sub **SetStock**( [CATIABase](../System/interface_AnyObject_17321.md)  `iStock`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Associates a stock to a Manufacturing Setup.
The stock must be either a Body feature (Geometrical Set, Ordered Geometrical Set, PartBody, Body.n) either a CGR product.

**Example:**     The following example associates the stock `iStock` belonging to the Product `iProduct` to the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.SetStock(iStock,iProduct)

```

### Sub **SetToolChangePoint**( double  `iX`,  double  `iY`,  double  `iZ`)

   Initialise the ToolChange point of the machine linked to a Manufacturing Setup.

**Example:**     The following example initialise the point with coordinates `X,Y,Z` as ToolChangePoint in the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.SetToolChangePoint(X,Y,Z)

```

### Sub **SetToolChangePointByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPointName`)

   Initialise the ToolChange point of the machine linked to a Manufacturing Setup.

**Example:**     The following example initialise the point `PT23` as ToolChangePoint in the manufacturing setup `CurrentSetup`

```VBScript
     call CurrentSetup.SetToolChangePointByName(PT23)

```

### Func **StockGeometriesCount**( ) As long

   Returns the number of stock geometries from a Manufacturing Setup.

**Parameters:**

` oStockGeometriesListSize`      The number of stock geometries of this setup  **Example:**     The following example retrieves the number of stock geometries of the setup `CurrentSetup` in `StockGeometriesListSize`.

```VBScript
     Dim CurrentSetup As ManufacturingSetup
     Set CurrentSetup = ...
     Dim StockGeometriesListSize As Long
     StockGeometriesListSize = CurrentSetup.StockGeometriesCount

```

---

# ManufacturingTool (Object)

**_A ManufacturingTool for a Manufacturing Document._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the Default Comment of a Manufacturing Setup.

**Example:**     The following example return the comment `ToolComment` of to the manufacturing tool `CurrentTool`

```VBScript
     ToolComment=CurrentTool.Comment

```

### Property **CorrectorCount**( ) As short (Read Only)

   Retreive the number of correctors of a Manufacturing tool.

**Example:**     The following example retreives in `CorrCount` the number of tool correctors of tool `CurrentTool`

```VBScript
     Set NbCorr = CurrentTool.CorrectorCount

```

### Property **NumberOfAttributes**( ) As short (Read Only)

   Give the Number og attributes of a Manufacturing Tool.

**Example:**     The following example returns the `Number` of attributes of the manufacturing Tool `CurrentTool`

```VBScript
     Number = CurrentTool.NumberOfAttributes

```

### Property **Picture**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the path where a picture of the parametrized tool is stored.

**Example:**     The following example return the path `PicturePath` where can be found the picture of the tool `CurrentTool`

```VBScript
     PicturePath=CurrentTool.Picture

```

### Property **ToolNumber**( ) As long (Read Only)

   Give the Number linked to a Manufacturing Tool.

**Example:**     The following example returns the `Number` linked to the manufacturing Tool `CurrentTool`

```VBScript
     Number = CurrentTool.ToolNumber

```

### Property **ToolType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the technological type of a the tool.

**Example:**     The following example return the tool type `ToolType` of to the manufacturing tool `CurrentTool`

```VBScript
     Set ToolType=CurrentTool.ToolType

```

Methods

### Func **AddCorrector**( ) As [CATIAManufacturingToolCorrector](../ManufacturingInterfaces/interface_ManufacturingToolCorrector_145356.md)

   Adds a corrector to a Manufacturing tool.

**Example:**     The following example adds in `Corr` the tool corrector of Tool `CurrentTool`

```VBScript
     Set Corr = CurrentTool.AddCorrector

```

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve by is name the attribute of a Manufacturing Tool.
Each attribute is a CKE object.

**Example:**     The following example retreives in `Diameter` the attribute `MfgDiameter` of the Manufacturing Tool `firstTool`

```VBScript
     Set Diameter = firstTool.GetAttribute(MfgDiameter)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieve the NLS name from the attribute name of a Manufacturing Tool.

### Func **GetCorrector**( short  `index`) As [CATIAManufacturingToolCorrector](../ManufacturingInterfaces/interface_ManufacturingToolCorrector_145356.md)

   Retreive the corrector (index) of a Manufacturing tool.

**Example:**     The following example retreives in `Corr` the tool corrector of Tool `CurrentTool`

```VBScript
     Set Corr = CurrentTool.GetCorrector(index)

```

### Sub **GetListOfAptParameters**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAptParameters`)

   Retrieve the list of apt definition parameters of a Manufacturing Tool.
Parameters are returned in an array of real values.

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributeUnits`)

   Retrieve the list of attribute units of a Manufacturing Tool.
The number of items in the output array is equal to the number of attributes of the tool.
When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.

**Example:**     The following example retrieves in `TabAttributeUnits` the list of attribute units of the Manufacturing Tool `firstTool`

```VBScript
     call firstTool.GetListOfAttributeUnits(TabAttributeUnits)

```

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of attributes of a Manufacturing Tool.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `TabAttributes` the list of attributes of the Manufacturing Tool `firstTool`

```VBScript
     call firstTool.GetListOfAttributes(TabAttributes)

```

### Sub **GetListOfGeomAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of geometry attributes of a Manufacturing Tool.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `TabGeomAttributes` the list of geometry attributes of the Manufacturing Tool `firstTool`

```VBScript
     call firstTool.GetListOfGeomAttributes(TabAttributes)

```

---

# ManufacturingToolAssembly (Object)

**_Represents the tool assembly._**

## Properties

### Property **AssemblyType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the type of the tool assembly.

**Legal values** : the type of the tool assembly can be either MfgMillAndDrillToolAssembly or MfgLatheToolAssembly.

**Example:**      The following example returns the assembly type `Type` of the assembly `CurrentAssembly`:

```VBScript
     Set Type=CurrentAssembly.AssemblyType

```

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the default comment of a tool assembly.

**Example:**      The following example returns the comment `Comment` of the tool assembly `CurrentAssembly`:

```VBScript
     Comment=CurrentAssembly.Comment

```

### Property **Insert**( ) As [CATIAManufacturingInsert](../ManufacturingInterfaces/interface_ManufacturingInsert_78415.md) (Read Only)

   Returns the insert of an assembly.

**Example:**      The following example retrieves in `Insert` the insert of the assembly `CurrentAssembly`:

```VBScript
     Set Insert = CurrentAssembly.Insert

```

### Property **NumberOfAttributes**( ) As short (Read Only)

   Returns the number of attributes of a tool assembly.

**Example:**      The following example returns the `Number` of attributes of the tool assembly `CurrentAssembly`:

```VBScript
     Number = CurrentAssembly.NumberOfAttributes

```

### Property **Tool**( ) As [CATIAManufacturingTool](../ManufacturingInterfaces/interface_ManufacturingTool_62710.md) (Read Only)

   Returns the tool of an assembly.

**Example:**      The following example retrieves in `Tool` the manufacturing tool of the assembly `CurrentAssembly`:

```VBScript
     Set Tool = CurrentAssembly.Tool

```

### Property **ToolNumber**( ) As long (Read Only)

   Returns the number linked to a tool assembly.

**Example:**      The following example returns the `Number` linked to the tool assembly `CurrentAssembly`:

```VBScript
     Number = CurrentAssembly.ToolNumber

```

Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribute`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Returns an attribute of a tool assembly.
The attribute is identified using its name, and is retrieved as a [Parameter](../KnowledgeInterfaces/interface_Parameter_17963.md) object.

**Parameters:**

` iAttribute`      The attribute name

**Returns:**      The retrieved attribute  **Example:**      The following example retrieves in `Diameter` the attribute `MfgDiameter` of the tool assembly `CurrentAssembly`:

```VBScript
     Set Diameter = CurrentAssembly.GetAttribute(MfgDiameter)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the NLS value of an attribute.

**Parameters:**

` iAttributeName`      The attribute name

**Returns:**      The attribute NLS value  **Example:**      The following example gives in `NLSresult` the NLS value of the "MFG_COMMENT" attributes of the tool assembly `CurrentAssembly`:

```VBScript
     NLSresult = CurrentAssembly.GetAttributeNLSName("MFG_COMMENT")

```

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioListOfAttributeUnits`)

   Retrieves the list of attribute units of a tool assembly.
The number of items in the output array is equal to the number of attributes of the assembly. When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.

**Parameters:**

` ioListOfAttributeUnits`      The retrieved list of attributes units

**Example:**      The following example retrieves in `TabAttributeUnits` the list of attribute units of the tool assembly `CurrentAssembly`:

```VBScript
     call CurrentAssembly.GetListOfAttributeUnits(TabAttributeUnits)

```

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioListOfAttributes`)

   Retrieves the list of attributes of a tool assembly.
Each attribute retrieved as a [Parameter](../KnowledgeInterfaces/interface_Parameter_17963.md) object.

**Parameters:**

` ioListOfAttributes`      The retrieved list of attributes

**Example:**      The following example retrieves in `TabAttributes` the list of attributes of the tool assembly `CurrentAssembly`:

```VBScript
     call CurrentAssembly.GetListOfAttributes(TabAttributes)

```

---

# ManufacturingToolCorrector (Object)

**_Manufacturing tool corrector._**

## Properties

### Property **Diameter**( ) As double (Read Only)

   Gives the corrector diameter tool diameter.
Returns HRESULT.

### Property **LengthNumber**( ) As short (Read Only)

   Gives the corrector length number.
Returns HRESULT.

### Property **Number**( ) As short (Read Only)

   Gives the corrector number.
Returns HRESULT.

### Property **Point**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Gives the corrector type point.
oPoint : Type point (Ex: P1, ..., P9)
Returns HRESULT.

### Property **RadiusNumber**( ) As short (Read Only)

   Gives the corrector radius number.
Returns HRESULT.
Methods

### Sub **GetValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPoint`,  short  `oNumber`,  short  `oLengthNumber`,  short  `oRadiusNumber`,  double  `oDiameter`)

   Gives the corrector values.
oPoint : Type point (Ex: P1, ..., P9)
oNumber : Corrector Number
oLengthNumber : Corrector Length Number
oRadiusNumber : Corrector Radius Number
oDiameter : Tool Diameter where corrector applyes (if non fixed corrector)
Returns HRESULT.

### Sub **SetValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPoint`,  short  `oNumber`,  short  `oLengthNumber`,  short  `oRadiusNumber`,  double  `oDiameter`)

   Defines the corrector values.
iPoint : Type point (Ex: P1, ..., P9)
iNumber : Corrector Number
iLengthNumber : Corrector Length Number
iRadiusNumber : Corrector Radius Number
iDiameter : Tool Diameter where corrector applyes (if non fixed corrector)
Returns HRESULT.

---

# ManufacturingToolMotion (Object)

**_A ManufacturingToolMotion for a Manufacturing Document._**

## Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve by is name the attribute of a Manufacturing ToolMotion.
Each attribute is a CKE object.

**Example:**     The following example retreives in `Diameter` the attribute `MfgDiameter` of the Manufacturing ToolMotion `firstToolmotion`

```VBScript
     Set Diameter = firstToolmotion.GetAttribute(MfgDiameter)

```

### Func **GetFeedrate**( double  `oFeedrate`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the Feedrate of a Manufacturing Point to point ToolMotion.
If the ToolMotion is not a Manufacturing Point to point, nothing is done.

**Parameters:**

` oFeedrateType`      **Legal values** : oFeedrateType can be:

`"RAPID"`     `"LOCAL"`     `"NONE"`
` oFeedrate`      Feedrate value. (expressed in MKS units : m/s if linear feedrate, or m/turn if angular feedrate)
Feedrate value has a meaning only if oFeedrateType is "LOCAL"  **Example:**     The following example gets the feedrate type of a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
     dim FeedVal as double
     dim FeedType as CATBSTR
     FeedType=SubMotion1.GetFeedrate(FeedVal)

```

### Sub **GetGotoPtPointCoordinates**( double  `oX`,  double  `oY`,  double  `oZ`)

   Retrieves coordinates on the ToolMotion.
If the type of the ToolMotion is not MfgSeqMotionPoint, nothing is done.
These coordinates are expressed in the current axis system.
Coordinates units are millimeters.

**Example:**     The following example gets coordinates on a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
     dim XCoord as double
     dim YCoord as double
     dim ZCoord as double
     Call SubMotion1.GetGotoPtPointCoordinates(XCoord, YCoord, ZCoord)

```

### Func **GetPPWord**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the content of a Manufacturing PP Word ToolMotion.

**Example:**     The following example retrieves in `Message` the content of the Manufacturing PPWord Toolmotion `firstToolmotion`

```VBScript
     dim Message as CATBSTR
     Message = firstToolmotion.GetPPWord

```

### Func **GetType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the type of a Manufacturing ToolMotion.

**Parameters:**

` oType`      **Legal values** : oType can be:

`"MfgSeqMotionPoint"`     `"MfgSeqMotionPosition"`     `"MfgSeqMotionDelta"`     **Example:**     The following example retrieves in `ThisType` the type of the Manufacturing Toolmotion `firstToolMotion`

```VBScript
     dim ThisType as CATBSTR
     Set ThisType = firstToolMotion.GetType

```

### Sub **SetFeedrate**( double  `iFeedrate`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`)

   Defines the feedrate of a Manufacturing Point to point ToolMotion.
If the ToolMotion is not a Manufacturing Point to point, nothing is done.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be:

`"RAPID"`     `"LOCAL"`     `"NONE"`
` oFeedrate`      Feedrate value. (expressed in MKS units : m/s if linear feedrate, or m/turn if angular feedrate)
Feedrate value is taken into account only if iFeedrateType is "LOCAL"  **Example:**     The following example sets a local feedrate on a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
     dim FeedVal as double
     dim FeedType as CATBSTR
     FeedVal = 169.0
     FeedType="LOCAL"
     Call SubMotion1.SetFeedrate(FeedVal, FeedType)

```

### Sub **SetGotoPtPointCoordinates**( double  `iX`,  double  `iY`,  double  `iZ`)

   Defines coordinates on the ToolMotion.
If the type of the ToolMotion is not MfgSeqMotionPoint, nothing is done.
These coordinates are expressed in the current axis system.
Coordinates units are millimeters.

**Example:**     The following example sets coordinates on a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
     dim XCoord as double
     dim YCoord as double
     dim ZCoord as double
     XCoord = 10.0
     YCoord = 20.0
     ZCoord = 5.0
     Call SubMotion1.SetGotoPtPointCoordinates(XCoord, YCoord, ZCoord)

```

### Sub **SetPPWord**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMessage`)

   Adds a line containing iMessage to a Manufacturing PP Word ToolMotion.

**Example:**     The following example adds the line `Message` to the content of the Manufacturing PPWord Toolmotion `firstToolmotion`

```VBScript
     firstToolmotion.SetPPWord("Message")

```

---

# ManufacturingView (Object)

**_The Manufacturing View is the object that holds all the manufacturing features of the model._**

## Properties

### Property **ManufacturingFeatures**( ) As [CATIAManufacturingFeatures](../ManufacturingInterfaces/interface_ManufacturingFeatures_95125.md) (Read Only)

   Returns the Manufacturing Features of a Manufacturing View.

**Example:**     The following example returns in `ManufacturingFeatures` the Manufacturing Features of the Manufacturing View `MfgView`:

```VBScript
     Set ManufacturingFeatures = MfgView.ManufacturingFeatures

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

   Returns the Relations Set owned by a Manufacturing View.

**Example:**     The following example returns in `Relations` the Relations Set of the Manufacturing View `MfgView`:

```VBScript
     Set Relations = MfgView.Relations

```

Methods

### Sub **CreateAllMachinableAreaFeaturesFromTechResultsOfUDF**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iFinishPartProduct`)

   Creates Machinable feature using TR of UDF.

**Example:**     The following example takes `iFinishPartProduct` and Create MAF in `MfgView`:

```VBScript
     MfgView.CreateAllMachinableAreaFeaturesFromTechResultsOfUDF(iFinishPartProduct)

```

---

# MfgActivities (Collection)

**_The collection of MfgActivities related to the Manufacturing Document ._**

## Methods

### Sub **Add**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iRealObj`)

   This method adds the specified CATIAManufacturingActivity in the current list CATIAMfgActivities.

**Example:**     The following example adds in CATIAMfgActivities `ListActivities` the CATIAManufacturingActivity `ThisActivity` in position `NumPos`:

```VBScript
     ListActivities.Add(ThisActivity)

```

### Func **GetElement**( long  `iIndex`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   This method return the specified CATIAManufacturingActivity in the current list CATIAMfgActivities.

**Example:**     The following example return the CATIAManufacturingActivity `ThisActivity` in CATIAMfgActivities `ListActivities` in position `NumPos`:

```VBScript
     Set ThisActivity = ListActivities.GetElement(Numpos)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   This method return the specified CATIAManufacturingActivity in the current list CATIAMfgActivities.

**Example:**     The following example return the CATIAManufacturingActivity `ThisActivity` in CATIAMfgActivities `ListActivities` in position `NumPos`:

```VBScript
     Set ThisActivity = ListActivities.Item(Numpos)

```

---

# MfgToolMotions (Collection)

**_The collection of MfgToolMotions related to the Manufacturing Document ._**

## Methods

### Sub **Add**( [CATIAManufacturingToolMotion](../ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)  `iRealObj`)

   This method adds the specified CATIAManufacturingToolMotion in the current list CATIAMfgToolMotions.

**Example:**     The following example adds in CATIAMfgToolMotions `ListToolMotions` the CATIAManufacturingToolMotion `ThisToolMotion`

```VBScript
     ListToolMotions.Add(ThisToolMotion)

```

### Func **GetElement**( long  `iIndex`) As [CATIAManufacturingToolMotion](../ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)

   This method return the specified CATIAManufacturingToolMotion in the current list CATIAMfgToolMotions.

**Example:**     The following example return the CATIAManufacturingToolMotion `ThisToolMotion` in CATIAMfgToolMotions `ListToolMotions` in position `NumPos`:

```VBScript
     Set ThisToolMotion = ListToolMotions.GetElement(Numpos)

```