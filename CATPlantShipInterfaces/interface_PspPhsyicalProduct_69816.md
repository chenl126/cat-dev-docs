# PspPhsyicalProduct (Object)

**_Represents the interface to manage the technological connectors on physical objects._**

**Role** : To manage connectors on physical objects.

## Properties

### Property **Connectors**(| ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of Part connectors of the object.

**Example:**

```VBScript
     Dim objThisIntf As PspPhsyicalProduct
     Dim objArg1 As PspListOfObjects
      ...
     Set objArg1 = objThisIntf.Connectors

```

Methods

### Func **AddConnector**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iClassFilter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieFaceType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAlignmentCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieAlignType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iClockCntr`,  [CatPspIDLPartConnectorType](../CATPlantShipInterfaces/enum_CatPspIDLPartConnectorType_138790.md)  `ieClockType`) As [CATIAPspPartConnector](../CATPlantShipInterfaces/interface_PspPartConnector_55256.md)

   Returns the added connector on the object.

**Parameters:**

` iuClassFilter`      Connector class type. If null string application default connector class will be used.
` iFaceCntr`      A face connector
` ieFaceType`      Face connector type
` iAlignmentCntr`      An alignment connector
` ieAlignType`      Alignment connector type
` iClockCntr`      A clock connector
` ieClockType`      A clock connector type

**Returns:**      Part connector added  **Example:**

```VBScript
     Dim objThisIntf As PspPhsyicalProduct

     Dim strVar1 As CATBSTR
     Dim objArg2 As Reference
     Dim objArg3 As catPspIDLPartConnectorType
     Dim objArg4 As Reference
     Dim objArg5 As catPspIDLPartConnectorType
     Dim objArg6 As Reference
     Dim objArg7 As catPspIDLPartConnectorType
     Dim objArg8 As PspPartConnector
      ...
     objArg8 = objThisIntf.AddConnector (strVar1, objArg2,objArg3,objArg4, objArg5,objArg6,objArg7 )

```

### Sub **RemoveConnector**( [CATIAPspPartConnector](../CATPlantShipInterfaces/interface_PspPartConnector_55256.md)  `iCntrToRemove`)

   Removes part connector.

**Parameters:**

` iCntrToRemove`      Part connector to be removed

**Example:**

```VBScript
     Dim objThisIntf As PspPhsyicalProduct

     Dim objArg1 As PspPartConnector
      ...
     objThisIntf.RemoveConnector objArg1

```