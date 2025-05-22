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