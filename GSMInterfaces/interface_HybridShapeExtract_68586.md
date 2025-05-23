# HybridShapeExtract (Object)

**_Represents the hybrid shape extract feature object._**

**Role** : To access the data of the hybrid shape extract feature object.

Use the CATIAHybridShapeFactory to create a HybridShapeExtract object.

**See also:**      [HybridShapeFactory.AddNewExtract](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewExtract)

## Properties

### Property **AngularThreshold**(| ) As double

   Returns or sets the AngularThreshold.

**Example** : This example retrieves the AngularThreshold of the `hybShpExtract` in `AngularThH`.

```VBScript
     Dim AngularThH as double
     AngularThH = hybShpExtract.AngularThreshold

```

### Property **AngularThresholdActivity**( ) As boolean

   Returns or sets the AngularThresholdActivity.

**Example** : This example retrieves the AngularThresholdActivity of the `hybShpExtract` in `AngularActivity `.

```VBScript
     Dim AngularActivity as boolean
     AngularActivity = hybShpExtract.AngularThresholdActivity

```

### Property **ComplementaryExtract**( ) As boolean

   Returns or sets the ComplementaryExtract checked/unchecked for the extract.  
### Property **CurvatureThreshold**( ) As double

   Returns or sets the CurvatureThreshold.

**Example** : This example retrieves the CurvatureThreshold of the `hybShpExtract` in `CurvatureThH`.

```VBScript
     Dim CurvatureThH as double
     CurvatureThH = hybShpExtract.CurvatureThreshold

```

### Property **CurvatureThresholdActivity**( ) As boolean

   Returns or sets the CurvatureThresholdActivity.

**Example** : This example retrieves the CurvatureThresholdActivity of the `hybShpExtract` in `CurvatureActivity `.

```VBScript
     Dim CurvatureActivity as boolean
     CurvatureActivity = hybShpExtract.CurvatureThresholdActivity

```

### Property **DistanceThreshold**( ) As double

   Returns or sets the DistanceThreshold.

**Example** : This example retrieves the DistanceThreshold of the `hybShpExtract` in `DistanceThH`.

```VBScript
     Dim DistanceThH as double
     DistanceThH = hybShpExtract.DistanceThreshold

```

### Property **DistanceThresholdActivity**( ) As boolean

   Returns or sets the DistanceThresholdActivity.

**Example** : This example retrieves the DistanceThresholdActivity of the `hybShpExtract` in `DistanceActivity `.

```VBScript
     Dim DistanceActivity as boolean
     DistanceActivity = hybShpExtract.DistanceThresholdActivity

```

### Property **Elem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the sub element used as init for the propagation.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **IsFederated**( ) As boolean

   Returns or sets the IsFederated flag checked/unchecked for the extract.  
### Property **PropagationType**( ) As long

   Returns or sets the type of propagation for the extract.
The propagation types for the extract can have the following values:

  * 1 for extraction propagation in point continuity
  * 2 for extraction propagation in tangent continuity
  * 3 for extraction without propagation

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support for the extract.