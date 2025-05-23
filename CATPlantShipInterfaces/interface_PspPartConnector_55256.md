# PspPartConnector (Object)

**_Represent the Part Connector to manage the technological data on connectors._**

**Role** : To access the technological data on connectors.

## Properties

### Property **AlignType**(| ) As [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) (Read Only)

   Returns the alignment type for this connector.

**See also:**      [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) **Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As CatPspIDLPartConnectorType

      ...
     objArg1 = objThisIntf.AlignType

```

### Property **AttributeNames**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

   Returns or sets a list of attribute names associated with this connector.

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim ojArg1 As PspListOfBSTRs
      ...
     Set ojArg1 = objThisIntf.AttributeNames

```

### Property **ClockType**( ) As [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) (Read Only)

   Returns the clocking type (how symmetric this end is) for this connector.

**See also:**      [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) **Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As CatPspIDLPartConnectorType

      ...
     objArg1 = objThisIntf.ClockType

```

### Property **FaceType**( ) As [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) (Read Only)

   Returns the face type (normal or "transparent" support) for this connector.

**Parameters:**

` oFaceType`      The face type.

**See also:**      [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md) **Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As CatPspIDLPartConnectorType

      ...
     Set objArg1 = objThisIntf.FaceType

```

Methods

### Func **GetAlignmentConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the Alignmnet connector.

**Parameters:**

` oCntr`      Alignment connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetAlignmentConnector

```

### Func **GetAlignmentDirection**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Retrieves the alignment direction outward normal to the face place position.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oAlignmentDirection`      Three double values stand for X,Y,Z components of the alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetAlignmentVector (objArg1)

```

### Func **GetConnectorMathPlane**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the 9 doubles values for plane contains the connector position (plane origin), alignment direction (plane z-axis), and the up direction (plane y-axis). Nine double values stand for plane origin, and the two normalized vectors

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetConnectorMathPlane (objArg1)

```

### Func **GetDatumConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the Datum connector.

**Parameters:**

` oCntr`      Orientation connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetDatumConnector

```

### Func **GetFaceConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the face connector.

**Parameters:**

` oCntr`      Face connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetFaceConnector

```

### Func **GetOrientationConnector**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Get Orientation connector.

**Parameters:**

` oCntr`      Orientation connector

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     Set objArg1 = objThisIntf.GetOrientationConnector

```

### Func **GetPosition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the Position of the connector.

**Parameters:**

` iRelAxis`      The relative axis object (NULL means relative to parent).
` oPosition`      X-Y-Z coordinates of the part connector Three double values stand for x,y,z coordinates

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetPosition (objArg1 )

```

### Func **GetUpDirection**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the UP direction of the connector.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).
` oUpDirection`      The connector face plane.

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetUpDirection (objArg1)

```

### Sub **SetAlignmentConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAlignCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieAlignType`)

   Sets the Face connector.

**Parameters:**

` iAlignCntr`      Alignment connector
` ieAlignType`      Alignment connector Type

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
     Dim objArg2 As CatPspIDLPartConnectorType
      ...
     objThisIntf.SetFaceConnector objArg1, objArg2

```

### Sub **SetDatumConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDatumCntr`)

   Sets the Datum connector.

**Parameters:**

` iDatumCntr`      Datum connector.

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
      ...
     objThisIntf.SetDatumConnector objArg1

```

### Sub **SetFaceConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieFaceType`)

   Sets Face connector.

**Parameters:**

` iFaceCntr`      Face connector
` ieFaceType`      Face connector Type

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
     Dim objArg2 As CatPspIDLPartConnectorType
      ...
     objThisIntf.SetFaceConnector objArg1, objArg2

```

### Sub **SetOrientationConnector**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iOrientCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieOrientation`)

   Sets Face connector.

**Parameters:**

` iOrientCntr`      Alignment connector
` ieOrientation`      Orientation connector Type

**Example:**

```VBScript
     Dim objThisIntf As PspPartConnector
     Dim objArg1 As Reference
     Dim objArg2 As CatPspIDLPartConnectorType
      ...
     objThisIntf.SetOrientationConnector objArg1, objArg2

```