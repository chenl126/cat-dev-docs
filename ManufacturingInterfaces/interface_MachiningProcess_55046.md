# MachiningProcess (Object)

**_MachiningProcess defines a set of properties and methods to apply a Machining Process to a geometrical feature (design or manufacturing)._**
It refers to a Machining Process which has been defined in the Machining Process view of a CATProcess file In the VB macro, be sure that the **active document** is the **target document** where are located the insertion level and where the instantiated activities will be created

## Properties

### Property **InsertionLevel**( ) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

This property defines the insertion level in the program receiving the resulting operations. It can be set to either the Manufacturing Program or one the Manufacturing Activities of the Manufacturing Program.

**Example:**     The following example sets the `InsertionLevel` property to the first Manufacturing Program as `ManufacturingActivity` Activity for the mpReference `MachiningProcess` which will be used for the Machining Process application:

```VBScript
...
Dim programReference As ManufacturingActivity
Set programReference = ...
Dim mpReference As MachiningProcess
Set mpReference = ...
mpReference.InsertionLevel = programReference

```

Methods

### Func **GetActivities**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)

This method gets the Manufacturing Activities referenced by the Machining Process.

**Parameters:**

` oMfgActivities`      The Manufacturing Activities list

### Func **InsertActivity**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iActivityType`,  [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iReferencedActivity`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

This method creates and inserts a Manufacturing Activity in the Machining Process.

**Parameters:**

` iActivityType`      The activity to be created type
` iReferencedActivity`      The insertion level in the machining process: the machining process itself to insert at the beginning of the Machining Process
` oManufacturingActivity`      The inserted activity

**Example:**     The following example executes the `InsertActivity` method to add a drilling operation to the mpReference `MachiningProcess`

```VBScript
...
Dim mpReference As MachiningProcess
Set mpReference = ...
...
Dim iActivityType As CATBSTR
Set iActivityType = Drilling
Dim iReferencedActivity As CATIAManufacturingActivity
Set iReferencedActivity = MachiningProcess
Dim oManufacturingActivity As CATIAManufacturingActivity
mpReference.InsertActivity(iActivityType,iReferencedActivity,oManufacturingActivity)

```

### Sub **Instantiate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeature`)

This method enables to apply a Machining Process to an any feature. This one has to be available for all Manufacturing Activities inside the Machining Process. At the end of the Machining Process application, the InsertionLevel property is set to the last created Manufacturing Activity in the Manufacturing program

**Example:**     The following example executes the `Instantiate` method to apply the mpReference `MachiningProcess` to a DesignFeature selected feature

```VBScript
...
Dim mpReference As MachiningProcess
Set mpReference = ...
...
Dim DesignFeature As AnyObject
Set DesignFeature = ...
...
mpReference.Instantiate(DesignFeature)

```

### Sub **InstantiateInProductContext**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeature`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

This method enables to apply a Machining Process to a given feature by taking into account the product from which it belongs to. This one has to be available for all Manufacturing Activities inside the Machining Process. At the end of the Machining Process application, the InsertionLevel property is set to the last created Manufacturing Activity in the Manufacturing program

**Parameters:**

` iFeature`      The feature on which the Machining Process is instantiated
` iProduct`      The product containing the feature.

**Example:**     The following example executes the `Instantiate` method to apply the mpReference `MachiningProcess` to a iDesignFeature selected feature

```VBScript
...
Dim mpReference As MachiningProcess
Set mpReference = ...
...
Dim iDesignFeature As AnyObject
Set iDesignFeature = ...
...
Dim iProduct As Product
Set iProduct = ...
...
mpReference.Instantiate(iDesignFeature,iProduct)

```