# SceneProductData (Object)

**_The interface to access a CATIASceneProduct

Using this prefered syntax will enable mkdoc to document your class._**

## Properties

### Property **Activation**( ) As boolean

Returns / Set the scene product's activation state.

**Example:**      This example retrieves the activation state of the `scenePrd` SceneProductData.

```VBScript
   IsActivated = scenePrd.Hidden

```

### Property **Hidden**( ) As boolean

Returns / Set the scene product's hide/show mode.

**Example:**      This example retrieves the hide/show mode of the `scenePrd` SceneProductData.

```VBScript
   IsHidden = scenePrd.Hidden

```

### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

Returns the scene product's move object. It aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves your product shape representation according to this isometry.

**Example:**      This example retrieves the `EngineMove` move in the `scenePrd` SceneProductData.

```VBScript
   Dim EngineMove As Move
   Set EngineMove = scenePrd.GetMove

```

### Property **Position**( ) As [CATIAPosition](../InfInterfaces/interface_Position_14692.md) (Read Only)

Returns the scene product's position object. The position object is the object aggregated by the SceneProductData object that holds the position of the master shape representation in the space in scene.

**Example:**      This example retrieves the `EnginePosition` position in the `scenePrd` SceneProductData.

```VBScript
   Dim EnginePosition As Position
   Set EnginePosition = scenePrd.GetPosition

```

Methods

### Sub **GetRealColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`,  long  `oInheritance`)

Returns / Set the scene product's color and inheritance.

**Parameters:**

` iRed`      A value between 0 and 255
` iGreen`      A value between 0 and 255
` iBlue`      A value between 0 and 255
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance
**Example:**      This example retrieves the activation state of the `scenePrd` SceneProductData.

```VBScript
    	Dim r, g, b, inh
   scenePrd.GetRealColor r, g, b, inh

```

### Sub **SetRealColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`,  long  `iInheritance`)

Returns / Set the scene product's color and inheritance.

**Parameters:**

` iRed`      A value between 0 and 255
` iGreen`      A value between 0 and 255
` iBlue`      A value between 0 and 255
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance
**Example:**      This example retrieves the activation state of the `scenePrd` SceneProductData.

```VBScript
   scenePrd.SetRealColor 255,0,0,1

```