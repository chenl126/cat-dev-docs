# PspObject (Object)

**_Represents PspObject._**
**Role** : To access Plant Ship object information.

## Properties

### Property **ApplicationID**( ) As [CatPspIDLApplicationID](../CATPlantShipInterfaces/enum_CatPspIDLApplicationID_94374.md) (Read Only)

Returns the ApplicationID of the object.

**Example:**

```VBScript
Dim objThisIntf As PspObject
Dim eApplID As CatPSPIDLApplicationID
 ...
eApplID = objThisIntf.ApplicationID

```

### Property **DomainID**( ) As [CatPspIDLDomainID](../CATPlantShipInterfaces/enum_CatPspIDLDomainID_53923.md) (Read Only)

Returns the DomainID of the object.

**Example:**

```VBScript
Dim objThisIntf As PspObject
Dim eDomanID As CatPspIDLDomainID
 ...
eDomanID = objThisIntf.DomainID

```

### Property **StartupType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the Startup type of the object.

**Example:**

```VBScript
Dim objThisIntf As PspObject
Dim strStartUp As String
...
strStartUp = objThisIntf.StartupType

```