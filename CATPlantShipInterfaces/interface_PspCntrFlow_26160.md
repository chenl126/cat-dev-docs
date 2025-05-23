# PspCntrFlow (Object)

**_Represents Interface to manage Connector Flow property._**

**Role** : To query and modify Plant-Ship Connector Flow property.

## Properties

### Property **FlowCapability**(| ) As [CatPspIDLFlowCapability](../CATPlantShipInterfaces/enum_CatPspIDLFlowCapability_107424.md)

   Returns or sets Flow capability of the connector.

**Example:**

```VBScript
     Dim objThisIntf As PspCntrFlow
     Dim ojArg1 As CatPspIDLFlowCapability
      ...
     Set ojArg1 = objThisIntf.FlowCapability

```

### Property **FlowReality**( ) As [CatPspIDLFlowReality](../CATPlantShipInterfaces/enum_CatPspIDLFlowReality_81334.md)

   Returns or sets Flow reality of the connector.

**Example:**

```VBScript
     Dim objThisIntf As PspCntrFlow
     Dim ojArg1 As CatPspIDLFlowReality
      ...
     Set ojArg1 = objThisIntf.FlowReality

```