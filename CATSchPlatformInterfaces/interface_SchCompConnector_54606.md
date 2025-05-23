# SchCompConnector (Object)

**_Manage the connectors of a schematic component._**

## Methods

### Sub **AddConnector**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iClassType`,| | [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md) | `iGRR`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iDb2CntrPosition`,| | [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md) | `oNewSchCntr`)

   Add a connector.

**Parameters:**

` iClassType`      Class type of the connector to be added.
` iGRR`      The graphical image of the component to add the connector to. If NULL, connector will be added to all representations.
` iDb2CntrPosition`      The position of the connector (optional, it could be NULL).
` oNewSchCntr`      The new Schematic Connector object created.

**Example:**

```VBScript
     Dim objThisIntf As SchCompConnector
     Dim strVar1 As String
     Dim objArg2 As SchGRRComp
     Dim dbVar3(2) As CATSafeArrayVariant
     Dim objArg4 As SchAppConnector
      ...
     objThisIntf.AddConnectorstrVar1,objArg2,dbVar3,objArg4

```

### Sub **AddDynamicConnector**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iClassType`,  [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2CntrPosition`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `oNewSchCntr`)

   Add a dynamic connector.

**Parameters:**

` iClassType`      Class type of the connector to be added.
` iGRR`      The graphical image of the component to add the connector to. If NULL, connector will be added to all representations.
` iDb2CntrPosition`      The position of the connector (optional, it could be NULL).
` oNewSchCntr`      The new Schematic Connector object created.

**Example:**

```VBScript
     Dim objThisIntf As SchCompConnector
     Dim strVar1 As String
     Dim objArg2 As SchGRRComp
     Dim dbVar3(2) As CATSafeArrayVariant
     Dim objArg4 As SchAppConnector
      ...
     objThisIntf.AddDynamicConnectorstrVar1,objArg2,dbVar3,objArg4

```

### Sub **RemoveConnector**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToRemove`)

   Remove a connector.

**Parameters:**

` iCntrToRemove`      The schematic connector object to be removed
` iGRR`      The graphical image of the component to remove the connector from. If NULL, connector will be removed from all representations.

**Example:**

```VBScript
     Dim objThisIntf As SchCompConnector
     Dim objArg1 As SchGRRComp
     Dim objArg2 As SchAppConnector
      ...
     objThisIntf.RemoveConnectorobjArg1,objArg2

```