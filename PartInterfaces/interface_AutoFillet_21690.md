# AutoFillet (Object)

**_Represents the AutoFillet shape._**
A AutoFillet fillets all the edges of Solid

## Properties

### Property **CurvatureRadius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Curvature radius.

**Example:**     The following example returns in `Curvature radius` the Curvature radius of the AutoFillet `Autofillet`:

```VBScript
Set Curvatureradius = Autofillet.Radius

```

### Property **FacesToFillet**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns or sets the faces to fillet.

**Example:**     The following example returns in `facestofillet` the faces required for autofillet `autoFillet`, and then sets it to `NewFacestofillet`:

```VBScript
Set Facestofillet = autoFillet.Facestofillet
autofillet.Facestofillet = NewFacestofillet

```

### Property **FacesToFillets**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`) (Write Only)

### Property **FilletRadius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Fillet radius.

**Example:**     The following example returns in `fillet radius` the fillet radius of the AutoFillet `Autofillet`:

```VBScript
Set Filletradius = Autofillet.Radius

```

### Property **FunctionalFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`) (Write Only)

### Property **FunctionalFaces**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns or sets the functional face.

**Example:**     The following example returns in `functionalface` the functional face of the autofillet `autoFillet`, and then sets it to `NewfunctionalFace`:

```VBScript
Set functionalFace = autoFillet.FunctionalFace
autofillet.FunctionalFace = NewfunctionalFace

```

### Property **PartingElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the parting element.

**Example:**     The following example returns in `partingelement` the parting element of the autofillet `autoFillet`, and then sets it to `Newparting element`:

```VBScript
Set Parting element = autoFillet.PartingElement
autofillet.PartingElement = NewPartingElement

```

### Property **RoundRadius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Round radius.

**Example:**     The following example returns in `round radius` the round radius of the AutoFillet `Autofillet`:

```VBScript
Set roundradius = Autofillet.Radius

```

### Property **RoundRadiusActivation**( ) As boolean

Returns the AutoFillet RoundRadiusActivation flag (for AutoFillet only).
It returns 1 if RoundRadius is activated, 0 if not.

**Returns:**      oRoundRadActivation The RoundRadActivation flag as an int

**Example:**
```

### Property **SliversAndCrack**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSlivers`) (Write Only)

### Property **SliversAndCracks**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns or sets the slivers face.

**Example:**     The following example returns in `slivers` the sliver face of the autofillet `autoFillet`, and then sets it to `Newsliver`:

```VBScript
Set sliversFace = autoFillet.SliversFace
autofillet.SliversFace = NewsliversFace

```

### Property **SupportSurface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support surface.

**Example:**     The following example returns in `SupportSurface` the support surface required for autofillet `autoFillet`, and then sets it to `NewSupportSurface`:

```VBScript
Set SupportSurface = autoFillet.SupportSurface
autofillet.SupportSurface = NewSupportSurface

```