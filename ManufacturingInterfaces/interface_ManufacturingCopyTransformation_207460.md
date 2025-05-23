# ManufacturingCopyTransformation (Object)

**_Interface representing the Manufacturing Copy Transformation object._**

**Role** : Component that implements CATIAManufacturingCopyOrder is MfgCopyOrder. This interface allows to modify the Copy Tranformation and to get the start and end points of the computed trajectory.

## Methods

### Sub **AddOperation**(| [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md) | `iManufacturingActivity`)

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