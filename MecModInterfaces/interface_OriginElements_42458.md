# OriginElements (Object)

**_Represents the part's 3D reference axis system._**
It allows an easy access to 3D reference axis system of a Part object thru the three planes XY, YZ, and ZX.
See [Part](../MecModInterfaces/interface_Part_3788.md) for parent object.

## Properties

### Property **PlaneXY**(| ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the XY plane of the part 3D reference axis system.

**Example:**     The following example returns in `plnXY` the XY plane of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set plnXY = partRoot.originElements.PlaneXY

```

### Property **PlaneYZ**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the YZ plane of the part 3D reference axis system.

**Example:**     The following example returns in `plnYZ` the YZ plane of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set plnYZ = partRoot.originElements.PlaneYZ

```

### Property **PlaneZX**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the ZX plane of the part 3D reference axis system.

**Example:**     The following example returns in `plnZX` the ZX plane of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set plnZX = partRoot.originElements.PlaneZX

```