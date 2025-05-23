# HybridShapeExtractMulti (Object)

**_Represents the hybrid shape ExtractMulti feature object._**

**Role** : To access the data of the hybrid shape ExtractMulti feature object.

Use the CATIAHybridShapeFactory to create a HybridShapeExtractMulti object.

**See also:**      [HybridShapeFactory.AddNewExtractMulti](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewExtractMulti)

## Methods

### Sub **AddConstraint**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iConstraint`,| | long | `iType`,| | boolean | `iComplementaire`,| | boolean | `iIsFederated`,| | double | `iCrvtreThsld`,| | long | `iPos`)

**Deprecated:**      V5R16 CATIAHybridShapeExtractMulti#AddConstraintTolerant Adds a constraint to the list of Extracted Elements.  **Parameters:**

` iConstraint`      The constraint to add.
` iType`      the type of propagation for the ExtractMulti.
` iComplementaire`      the Complementary flag checked/unchecked for for the constraint.
` iIsFederated`      the Federated flag checked/unchecked for the constraint.
` iCrvtreThsld`      the CurvatureThreshold for the constraint.
` iPos`      The position at which the element is to be added in the list of constraints.

**Example** :      This example adds a body in the list of constraints at specified position with the type of propagation, the Federated flag and the CurvatureThreshold of the `HybShpExtractMulti` hybrid shape ExtractMulti.

```VBScript
     Dim iType as long
     Dim iComplementaire as boolean
     Dim iIsFederated as boolean
     Dim iCrvtreThsld as double
     HybShpExtractMulti.AddConstraint iCst  iType  iComplementaire iIsFederated iCrvtreThsld  1

```

### Sub **AddConstraintTolerant**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iConstraint`,  long  `iType`,  boolean  `iComplementaire`,  boolean  `iIsFederated`,  double  `iDistreThsld`,  double  `iAngtreThsld`,  double  `iCrvtreThsld`,  long  `iPos`)

   Adds a constraint to the list of Extracted Elements.

**Parameters:**

` iConstraint`      The constraint to add.
` iType`      the type of propagation for the ExtractMulti.
` iComplementaire`      the Complementary flag checked/unchecked for for the constraint.
` iIsFederated`      the Federated flag checked/unchecked for the constraint.
` iDistreThsld`      the DistanceThreshold for the constraint.
` iAngtreThsld`      the AngularThreshold for the constraint.
` iCrvtreThsld`      the CurvatureThreshold for the constraint.
` iPos`      The position at which the element is to be added in the list of constraints.

**Example** :      This example adds a body in the list of constraints at specified position with the type of propagation, the Federated flag and the CurvatureThreshold of the `HybShpExtractMulti` hybrid shape ExtractMulti.

```VBScript
     Dim iType as long
     Dim iComplementaire as boolean
     Dim iIsFederated as boolean
     Dim iDistreThsld as double
     Dim iAngtreThsld as double
     Dim iCrvtreThsld as double
     HybShpExtractMulti.AddConstraintTolerant iCst  iType  iComplementaire iIsFederated iCrvtreThsld  1

```

### Func **GetAngularThreshold**( long  `iPos`) As double

   Returns the AngularThreshold of the list of constraints at specified position.

**Example** :      This example retrieves the AngularThreshold in the list of constraints at specified position of the `hybShpExtractMulti` in `AngularThH`.

```VBScript
     Dim oAngtreThsld as double
     AngularThH = HybShpExtractMulti.GetAngularThreshold(1)

```

### Func **GetAngularThresholdActivity**( long  `iPos`) As boolean

   Returns the AngularThresholdActivity of the list of constraints at specified position.

**Example** :      This example retrieves the AngularThresholdActivity of the list of constraints at specified position of the `hybShpExtractMulti` in `AngularActivity `.

```VBScript
     Dim oAngtreThsldActivity as boolean
     oAngtreThsldActivity  = HybShpExtractMulti.GetAngularThresholdActivity (1)

```

### Func **GetComplementaryExtractMulti**( long  `iPos`) As boolean

   Returns the Complementary flag checked/unchecked of the list of constraints at specified position.

**Example** :      This example retrieves the Complementary flag in the list of constraints at specified position of the `hybShpExtractMulti` in `Complementaire`.

```VBScript
     Dim oComplementaire as boolean
     oComplementaire  = HybShpExtractMulti.GetComplementaryExtractMulti(1)

```

### Func **GetCurvatureThreshold**( long  `iPos`) As double

   Returns the CurvatureThreshold of the list of constraints at specified position.

**Example** :      This example retrieves the CurvatureThreshold in the list of constraints at specified position of the `hybShpExtractMulti` in `CurvatureThH`.

```VBScript
     Dim oCrvtreThsld as double
     CurvatureThH = HybShpExtractMulti.GetCurvatureThreshold(1)

```

### Func **GetCurvatureThresholdActivity**( long  `iPos`) As boolean

   Returns the CurvatureThresholdActivity of the list of constraints at specified position.

**Example** :      This example retrieves the CurvatureThresholdActivity of the list of constraints at specified position of the `hybShpExtractMulti` in `CurvatureActivity `.

```VBScript
     Dim oCrvtreThsldActivity as boolean
     oCrvtreThsldActivity  = HybShpExtractMulti.GetCurvatureThresholdActivity (1)

```

### Func **GetDistanceThreshold**( long  `iPos`) As double

   Returns the DistanceThreshold of the list of constraints at specified position.

**Example** :      This example retrieves the DistanceThreshold in the list of constraints at specified position of the `hybShpExtractMulti` in `DistanceThH`.

```VBScript
     Dim oDistreThsld as double
     DistanceThH = HybShpExtractMulti.GetDistanceThreshold(1)

```

### Func **GetDistanceThresholdActivity**( long  `iPos`) As boolean

   Returns the DistanceThresholdActivity of the list of constraints at specified position.

**Example** :      This example retrieves the DistanceThresholdActivity of the list of constraints at specified position of the `hybShpExtractMulti` in `DistanceActivity `.

```VBScript
     Dim oDistreThsldActivity as boolean
     oDistreThsldActivity  = HybShpExtractMulti.GetDistanceThresholdActivity (1)

```

### Func **GetElement**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the sub element used as init for the propagation.

**Example** :      This example retrieves the sub element in the list of constraints at specified position of the `hybShpExtractMulti` in `Elem`.

```VBScript
     Dim oElem as CATIAReference
     oElem = HybShpExtractMulti.GetElement(1)

```

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Func **GetIsFederated**( long  `iPos`) As boolean

   Returns the IsFederated flag checked/unchecked of the list of constraints at specified position.

**Example** :      This example retrieves the federated flag in the list of constraints at specified position of the `hybShpExtractMulti` in `IsFederated`.

```VBScript
     Dim oIsFederated as boolean
     oIsFederated  = HybShpExtractMulti.GetIsFederated(1)

```

### Sub **GetListOfConstraints**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfExtractedConstraints`)

   Returns the list of Extracted Elements.

**Parameters:**

` oListOfExtractedConstraints`      The list of constraints. It is returned as an array of nbconstraints in SafeArrayVariant.

**Example** :      This example returns the list of constraints of the `HybShpExtractMulti` hybrid shape ExtractMulti.

```VBScript
     Dim oListOfExtractedConstraints as CATSafeArrayVariant
     HybShpExtractMulti.GetListOfConstraints (oListOfExtractedConstraints)

```

Note: You can access each constraint as follows:

  * `1` is in `oListOfExtractedConstraints(0)`
  * `2` is in `oListOfExtractedConstraints(1)`
  * `nbconstraints` is in `oListOfExtractedConstraints(nbconstraints-1)`

### Sub **GetNbConstraints**( long  `oNbConstraints`)

   Returns number of constraints in the list of Extracted Elements.

**Parameters:**

` oNbConstraints`      number of constraints in the list of Extracted Elements.

**Example** :      This example returns number of constraints in the list of constraints of the `HybShpExtractMulti` hybrid shape ExtractMulti.

```VBScript
     Dim oNbConstraints as long
     HybShpExtractMulti.GetNbConstraints (oNbConstraints )

```

### Func **GetPropagationType**( long  `iPos`) As long

   Returns the type of propagation of the list of constraints at specified position.
The propagation types for the ExtractMulti can have the following values:

  * 1 for extraction propagation in point continuity
  * 2 for extraction propagation in tangent continuity
  * 3 for extraction without propagation
  * 4 for extraction propagation in curvature continuity

**Example** :      This example retrieves the PropagationType in the list of constraints at specified position of the `hybShpExtractMulti` in `TypePropag`.

```VBScript
     Dim oTypePropag as long
     oTypePropag  = HybShpExtractMulti.GetPropagationType(1)

```

### Func **GetSupport**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the support of the list of constraints at specified position.

**Parameters:**

` oSupport`      The support.

### Sub **RemoveElement**( long  `iPosition`)

   Removes the body to be extracted from the list of constraints at specified position.

**Parameters:**

` iPosition`      Position at which the body is to be removed

**Example** :      This example removes the body from the list of constraints at specified position of the `HybShpExtractMulti` hybrid shape ExtractMulti.

```VBScript
     HybShpExtractMulti.RemoveElement  1

```

### Sub **ReplaceElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iExtractToReplace`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNewExtract`,  long  `iPos`)

   Replaces an element to extract in the list of constraints at specified position.

**Parameters:**

` iExtractToReplace`      The element to replace.
` iNewExtract`      The new element.
` iPos`      The position at which the element is to be replaced in the list of constraints.

**Example** :      This example replaces the body from the list of constraints at specified position of the `HybShpExtractMulti` hybrid shape ExtractMulti.

```VBScript
     Dim RefToRep  as CATIAReference
     Dim RefNewExtract  as CATIAReference
     HybShpExtractMulti.ReplaceElement RefToRep  RefNewExtract 1

```

### Sub **SetAngularThreshold**( long  `iPos`,  double  `iAngtreThsld`)

   Sets the AngularThreshold in the list of constraints at specified position.

**Example** :      This example sets the AngularThreshold of the list of constraints at specified position of the `hybShpExtractMulti` in `AngularThH`.

```VBScript
     Dim iAngtreThsld as double
     HybShpExtractMulti.SetAngularThreshold 1 iAngtreThsld

```

### Sub **SetAngularThresholdActivity**( long  `iPos`,  boolean  `iAngtreThsldActivity`)

   Sets the AngularThresholdActivity in the list of constraints at specified position.

**Example** :      This example sets the AngularThresholdActivity in the list of constraints at specified position of the `hybShpExtractMulti` in `AngularActivity `.

```VBScript
     Dim iAngtreThsldActivity as boolean
     iAngtreThsldActivity = TRUE
     HybShpExtractMulti.SetAngularThresholdActivity 1  iAngtreThsldActivity

```

### Sub **SetComplementaryExtractMulti**( long  `iPos`,  boolean  `iComplementaire`)

   Sets the Complementary flag checked/unchecked in the list of constraints at specified position.

**Example** :      This example sets the Complementary flag of the list of constraints at specified position of the `hybShpExtractMulti` in `Complementaire`.

```VBScript
     Dim iComplementaire as boolean
     iComplementaire  = TRUE
     HybShpExtractMulti.SetComplementaryExtractMulti 1   iComplementaire

```

### Sub **SetCurvatureThreshold**( long  `iPos`,  double  `iCrvtreThsld`)

   Sets the CurvatureThreshold in the list of constraints at specified position.

**Example** :      This example sets the CurvatureThreshold of the list of constraints at specified position of the `hybShpExtractMulti` in `CurvatureThH`.

```VBScript
     Dim iCrvtreThsld as double
     HybShpExtractMulti.SetCurvatureThreshold 1 iCrvtreThsld

```

### Sub **SetCurvatureThresholdActivity**( long  `iPos`,  boolean  `iCrvtreThsldActivity`)

   Sets the CurvatureThresholdActivity in the list of constraints at specified position.

**Example** :      This example sets the CurvatureThresholdActivity in the list of constraints at specified position of the `hybShpExtractMulti` in `CurvatureActivity `.

```VBScript
     Dim iCrvtreThsldActivity as boolean
     iCrvtreThsldActivity = TRUE
     HybShpExtractMulti.SetCurvatureThresholdActivity 1  iCrvtreThsldActivity

```

### Sub **SetDistanceThreshold**( long  `iPos`,  double  `iDistreThsld`)

   Sets the DistanceThreshold in the list of constraints at specified position.

**Example** :      This example sets the DistanceThreshold of the list of constraints at specified position of the `hybShpExtractMulti` in `DistanceThH`.

```VBScript
     Dim iDistreThsld as double
     HybShpExtractMulti.SetDistanceThreshold 1 iDistreThsld

```

### Sub **SetDistanceThresholdActivity**( long  `iPos`,  boolean  `iDistreThsldActivity`)

   Sets the DistanceThresholdActivity in the list of constraints at specified position.

**Example** :      This example sets the DistanceThresholdActivity in the list of constraints at specified position of the `hybShpExtractMulti` in `DistanceActivity `.

```VBScript
     Dim iDistreThsldActivity as boolean
     iDistreThsldActivity = TRUE
     HybShpExtractMulti.SetDistanceThresholdActivity 1  iDistreThsldActivity

```

### Sub **SetElement**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`)

   Sets the sub element used as init for the propagation.

**Example** :      This example sets the sub element in the list of constraints at specified position of the `hybShpExtractMulti` in `Elem`.

```VBScript
     Dim iPos as long
     Dim iElem as CATIAReference
     HybShpExtractMulti.SetElement 1 iElem

```

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetIsFederated**( long  `iPos`,  boolean  `iIsFederated`)

   Sets the IsFederated flag checked/unchecked in the list of constraints at specified position.

**Example** :      This example sets the federated flag in the list of constraints at specified position of the `hybShpExtractMulti` in `IsFederated`.

```VBScript
     Dim iIsFederated as boolean
      iIsFederated = TRUE
     HybShpExtractMulti.SetIsFederated 1  iIsFederated

```

### Sub **SetPropagationType**( long  `iPos`,  long  `iTypePropag`)

   Sets the type of propagation for the ExtractMulti in the list of constraints at specified position.
The propagation types for the ExtractMulti can have the following values:

  * 1 for extraction propagation in point continuity
  * 2 for extraction propagation in tangent continuity
  * 3 for extraction without propagation
  * 4 for extraction propagation in curvature continuity

**Example** :      This example sets the PropagationType of the list of constraints at specified position of the `hybShpExtractMulti` in `TypePropag`.

```VBScript
     Dim iTypePropag as long
     iTypePropag = 1
     HybShpExtractMulti.SetPropagationType 1 iTypePropag

```

### Sub **SetSupport**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Sets the support of the list of constraints at specified position.

**Parameters:**

` oSupport`      The support.