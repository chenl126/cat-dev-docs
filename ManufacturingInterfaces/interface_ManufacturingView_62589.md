# ManufacturingView (Object)

**_The Manufacturing View is the object that holds all the manufacturing features of the model._**

## Properties

### Property **ManufacturingFeatures**( ) As [CATIAManufacturingFeatures](../ManufacturingInterfaces/interface_ManufacturingFeatures_95125.md) (Read Only)

Returns the Manufacturing Features of a Manufacturing View.

**Example:**     The following example returns in `ManufacturingFeatures` the Manufacturing Features of the Manufacturing View `MfgView`:

```VBScript
Set ManufacturingFeatures = MfgView.ManufacturingFeatures

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

Returns the Relations Set owned by a Manufacturing View.

**Example:**     The following example returns in `Relations` the Relations Set of the Manufacturing View `MfgView`:

```VBScript
Set Relations = MfgView.Relations

```

Methods

### Sub **CreateAllMachinableAreaFeaturesFromTechResultsOfUDF**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iFinishPartProduct`)

Creates Machinable feature using TR of UDF.

**Example:**     The following example takes `iFinishPartProduct` and Create MAF in `MfgView`:

```VBScript
MfgView.CreateAllMachinableAreaFeaturesFromTechResultsOfUDF(iFinishPartProduct)

```