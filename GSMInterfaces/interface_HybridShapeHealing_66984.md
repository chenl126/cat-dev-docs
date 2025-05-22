# HybridShapeHealing (Object)

**_Represents the hybrid shape healing feature object._**
**Role** : Allows to access to the body to process for a Healing feature. Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory.AddNewHealing](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewHealing)

## Properties

### Property **CanonicFreeMode**( long  `iMode`)

Returns or sets the Canonic Free Mode of the healing.

**Parameters:**

` oMode`      (For get_CanonicFreeMode) Long parameter for retrieving the CanonicFreeMode.
` iMode`      (For set_CanonicFreeMode) Long parameter for settingthe CanonicFreeMode.

**Example** :      This example sets and retrieves the CanonicFreeMode of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealMode As  Long
HybShpHealMode = ..set appropriate value
HybShpHealing.CanonicFreeMode = HybShpHealMode
HybShpHealCont = HybShpHealing.CanonicFreeMode

```

### Property **Continuity**( long  `iContinuity`)

Returns or sets the continuity type of the healing.

**Parameters:**

` Continuity`      Parameter for the continuity. Legal values are 0 and 1

**Example** :      This example sets and retrieves the Continuity of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealCont As  Long
HybShpHealCont = ..set appropriate value
HybShpHealing.Continuity = HybShpHealCont
HybShpHealCont = HybShpHealing.Continuity

```

### Property **DistanceObjective**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Distance Objective of the healing.

**Parameters:**

` DistanceObjective`      Length parameter for retrieving the Distance Objective.

**Example** :      This example retrieves the DistanceObjective of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealDistObjective As Length
Set HybShpHealDistObjective = HybShpHealing.DistanceObjective

```

### Property **MergingDistance**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Merging Distance of the healing.

**Parameters:**

` MergingDistance`      Length parameter for retrieving the Merging Distance.

**Example** :      This example retrieves the MergingDistance of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealMergeDist As Length
Set HybShpHealMergeDist = HybShpHealing.MergingDistance

```

### Property **NoOfBodiesToHeal**( ) As long (Read Only)

Returns the number of bodies to heal of the healing.

**Parameters:**

` NumberOfbodies`      Number of bodies to heal in the healing.

**Example** :      This example retrieves the number of bodies to heal of the `HybShpHealing` hybrid shape Healing.

```VBScript
Dim NoOfBodiesToHeal As  long
NoOfBodiesToHeal = HybShpHealing.NoOfBodiesToHeal

```

### Property **NoOfEdgesToKeepSharp**( ) As long (Read Only)

Returns the number of edges to keep sharp of the healing.

**Parameters:**

` NumberOfEdges`      Number of edges to keep sharp.

**Example** :      This example retrieves the number of edges to keep sharp of the `HybShpHealing` hybrid shape Healing.

```VBScript
Dim NoOfEdges As  long
NoOfEdges = HybShpHealing.NoOfEdgesToKeepSharp

```

### Property **NoOfElementsToFreeze**( ) As long (Read Only)

Returns the number of elements to heal of the healing.

**Parameters:**

` NumberOfElements`      Number of elements to freeze in the healing.

**Example** :      This example retrieves the number of elements to freeze of the `HybShpHealing` hybrid shape Healing.

```VBScript
Dim NoOfElementsToFreeze As  long
NoOfElementsToFreeze = HybShpHealing.NoOfElementsToFreeze

```

### Property **SharpnessAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the Sharpness Angle of the healing.

**Parameters:**

` SharpnessAngle`      Angle parameter for retrieving the Sharpness Angle.

**Example** :      This example retrieves the Sharpness Angle of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealSharpnessAngle As Angle
Set HybShpHealSharpnessAngle = HybShpHealing.SharpnessAngle

```

### Property **TangencyAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the Tangency Angle of the healing.

**Parameters:**

` TangencyAngle`      Angle parameter for retrieving the TangencyAngle.

**Example** :      This example retrieves the TangencyAngle of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealTangencyAngle As Angle
Set HybShpHealTangencyAngle = HybShpHealing.TangencyAngle

```

### Property **TangencyObjective**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Tangency Objective of the healing.

**Parameters:**

` TangencyObjective`      Length parameter for retrieving the Tangency Objective.

**Example** :      This example retrieves the TangencyObjective of the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
Dim HybShpHealTangencyObjective As Length
Set HybShpHealTangencyObjective = HybShpHealing.TangencyObjective

```

Methods

### Sub **AddBodyToHeal**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody`)

Adds the body to be healed to the list.

**Parameters:**

` Body`      Reference to the body to be added to the list.

**Example** :      This example adds the body to the list. of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.AddBodyToHeal refBody

```

### Sub **AddEdgeToKeepSharp**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdge`)

Adds the edge to be kept sharp while healing, to the list.

**Parameters:**

` Edge`      Reference to the Edge to be kept sharp

**Example** :      This example adds the Edge to the list of Edges to be kept sharp. of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.AddEdgeToKeepSharp refEdge

```

### Sub **AddElementsToFreeze**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

Adds the body to be freezed while healing, to the list.

**Parameters:**

` Element`      Reference to the element to be freezed.

**Example** :      This example adds the body to the list of bodies to be freezed. of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.AddElementsToFreeze refElement

```

### Func **GetBodyToHeal**( long  `iPosition`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns the body to be healed from the list at specified position.

**Parameters:**

` Position`      Position at which the body is to be obtained
` Body`      Reference to the body obtained at specified position.

**Example** :      This example gets the body from the list by specifying the position. of the `HybShpHealing` hybrid shape healing.

```VBScript
set refBody = HybShpHealing.GetBodyToHeal  1

```

### Func **GetEdgeToKeepSharp**( long  `iPosition`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns the edge to be kept sharp from the list at specified position.

**Parameters:**

` Position`      Position at which the element is to be obtained
` Edge`      Reference to the element obtained at specified position.

**Example** :      This example gets the Edge from the list of Edges to be kept sharp by specifying the position of the `HybShpHealing` hybrid shape healing.

```VBScript
set refEdge = HybShpHealing.GetEdgeToKeepSharp  1

```

### Func **GetElementToFreeze**( long  `iPosition`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns the element to be freezed from the list at specified position.

**Parameters:**

` Position`      Position at which the element is to be obtained
` Element`      Reference to the element obtained at specified position.

**Example** :      This example gets the element from the list of bodies to be freezed by specifying the position of the `HybShpHealing` hybrid shape healing.

```VBScript
set refElement = HybShpHealing.GetElementToFreeze  1

```

### Sub **RemoveBodyToHeal**( long  `iPosition`)

Removes the body to be healed from the list at specified position.

**Parameters:**

` iPosition`      Position at which the body is to be removed

**Example** :      This example removes the body from the list at specifying the position. of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.RemoveBodyToHeal  1

```

### Sub **RemoveEdgeToKeepSharp**( long  `iPosition`)

Removes the edge from the list of edges to be kept sharp at specified position.

**Parameters:**

` iPosition`      Position at which the edge is to be removed

**Example** :      This example removes the edge from the list at specified position. of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.RemoveEdgeToKeepSharp  1

```

### Sub **RemoveElementToFreeze**( long  `iPosition`)

Removes the element from the list of elements to be freezed at specified position.

**Parameters:**

` Position`      Position at which the element is to be removed

**Example** :      This example removes the element from the list at specifying the position. of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.RemoveElementToFreeze  1

```

### Sub **ReplaceToHealElement**( long  `iIndex`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNewHeal`)

Replaces an element to heal.

**Parameters:**

` iIndex`      The position of the element to replace.
` iNewHeal`      The new element.

### Sub **SetDistanceObjective**( double  `iDistanceObjective`)

Sets the distance objective for healing entity.

**Parameters:**

` DistanceObjective`      Parameter containg the value of the distance objective to be set.

**Example** :      This example sets the distance objective for the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.SetDistanceObjective 2.5

```

### Sub **SetMergingDistance**( double  `iMergingDistance`)

Sets the Merging distance for healing entity.

**Parameters:**

` MergingDistance`      Parameter containg the value of the merging distance to be set.

**Example** :      This example sets the merging distance for the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.SetMergingDistance 2.5

```

### Sub **SetSharpnessAngle**( double  `iSharpnessAngle`)

Sets the Sharpness Angle for healing entity.

**Parameters:**

` SharpnessAngle`      Parameter containg the value of the Sharpness Angle to be set.

**Example** :      This example sets the Sharpness Angle for the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.SetSharpnessAngle 2.5

```

### Sub **SetTangencyAngle**( double  `iTangencyAngle`)

Sets the distance objective for healing entity.

**Parameters:**

` TangencyAngle`      Parameter containg the value of the Tangency Angle to be set.

**Example** :      This example sets the Tangency Angle for the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.SetTangencyAngle 2.5

```

### Sub **SetTangencyObjective**( double  `iTangencyObjective`)

Sets the tangency objective for healing entity.

**Parameters:**

` TangencyObjective`      Parameter containg the value of the Tangency Objective to be set.

**Example** :      This example sets the Tangency Objective for the healing of the `HybShpHealing` hybrid shape healing.

```VBScript
HybShpHealing.SetTangencyObjective 2.5

```