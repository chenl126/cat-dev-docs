# HybridShapeIntegratedLaw (Object)

**_Represents the hybrid shape "integrated" law feature object._**

**Role** : To access the data of the hybrid shape "integrated" law feature object.

Use the CATIAHybridShapeFactory to create a HybridShapeIntegratedLaw object.

**See also:**      [HybridShapeFactory.AddNewIntegratedLaw](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewIntegratedLaw)

## Properties

### Property **AdvancedLaw**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets or sets the external law.
Note: Used for law type = 4(Advanced)

**Parameters:**

` AdvancedLaw`      External Law This example retrieves in `ALaw` the external law for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim ALaw
     Set ALaw = IntegratedLaw.AdvancedLaw

```

### Property **EndParam**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Gets end parameter.
Note: Used for law type = 2(Linear) and 3(SType).

**Parameters:**

` EndParam`      Parameter This example retrieves in `EParam` the end parameter for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim EParam
     Set EParam = IntegratedLaw.EndParam

```

### Property **ImplicitLawInterpolationMode**( ) As long

   Gets or sets Interpolation mode for implicit law.
Note: Used for law type = 5(Implicit)

**Parameters:**

` ImplicitLawInterpolationMode`      Implicit law interpolation mode ImplicitLawInterpolationMode = 0 : CATGSMImplicitLawInterpo_None = 1 : CATGSMImplicitLawInterpo_Linear = 2 : CATGSMImplicitLawInterpo_Cubic This example retrieves in `InterpolLawMode` the Interpolation mode for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim InterpolLawMode
     Set InterpolLawMode = IntegratedLaw.ImplicitLawInterpolationMode

```

### Property **InvertMappingLaw**( ) As boolean

   Gets or sets the mapping orientation of the law.

**Parameters:**

` InvertMappingLaw`      False : Law is applied from the beginning to the end of the curve (mapping is not inverted).
True : Law is applied from the end to the beginning of the curve (mapping is inverted). This example retrieves in `IMappingLaw` the mapping orientation of the law for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim IMappingLaw
     Set IMappingLaw = IntegratedLaw.InvertMappingLaw

```

### Property **PitchLawType**( ) As long

   Gets or sets pitch law type.

**Parameters:**

` PitchLawType`      Type of law PitchLawType = 0 : None = 1 : Constant = 2 : Linear = 3 : SType = 4 : Advanced = 5 : Implicit This example retrieves in `PLawType` the pitch law type for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim PLawType
     Set PLawType = IntegratedLaw.PitchLawType

```

### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets or sets Spine for implicit law.
Note: Used for law type = 5 (Implicit)

**Parameters:**

` Spine`      Spine on which implicit law inputs points are defined This example retrieves in `Spine1` the spine for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim Spine1
     Set Spine1 = IntegratedLaw.Spine

```

### Property **StartParam**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Gets start parameter.
Note: Used for law type = 1(Constant) ,2(Linear) and 3(SType)

**Parameters:**

` StartParam`      Parameter This example retrieves in `SParam` the start parameter for the `IntegratedLaw` hybrid shape feature.

```VBScript
     Dim SParam
     Set SParam = IntegratedLaw.StartParam

```

Methods

### Sub **AppendNewPointAndParam**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  long  `iParam`)

   Sets 'Point on spine' and associated parameter.
Note: Used for law type = 5(Implicit)

**Parameters:**

` iPoint`      Point on spine
` iParam`      Corresponding parameter

### Sub **GetPointAndParam**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oParam`)

   Gets the point on spine and associated parameter at a given position.
Note: Used for law type = 5(Implicit)

**Parameters:**

` iPos`      given position
` oPoint`      point on spine
` oParam`      corresponding parameter

### Func **GetSize**( ) As long

   Gets the size of the list in the law i.e. number of points in the list of the law.

**Parameters:**

` oSize`      size of the list.

### Sub **RemoveAllPointsAndParams**( )

   Removes all the points and associated parameters.
Note: Used for law type = 5(Implicit)  
### Sub **RemovePointAndParam**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

   Removes a point and its parameter. for law type = 5(Implicit)

**Parameters:**

` iSpecPoint`      Point to remove

### Sub **SetEndParam**( long  `iEndParam`)

   Sets end parameter.
Note: Used for law type = 2(Linear) and 3(SType).

**Parameters:**

` iEndParam`      Parameter

### Sub **SetStartParam**( long  `iStartParam`)

   Sets start parameter.
Note: Used for law type = 1(Constant) ,2(Linear) and 3(SType).

**Parameters:**

` iStartParam`      Parameter