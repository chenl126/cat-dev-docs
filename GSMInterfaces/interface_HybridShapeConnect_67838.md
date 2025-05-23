# HybridShapeConnect (Object)

**_Represents the hybrid shape connect curve object._**

**Role** : To access the data of the hybrid shape connect curve object. This data includes:

  * The face to process
  * The connection parameter.

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) to create a HybridShapeConnect object.

## Properties

### Property **BaseCurve**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the base curve.

**Do not use this property** 
### Property **ConnectType**( ) As long

   Returns or sets whether the connect curve is or should be created as a"Normal Connect" or with a "Base Curve".

**Legal values** : 0 for the normal solution and 1 for base curve solution.

**Example:**      This example sets the mode to create the connect curve `hybConnectCurve` with a base curve.

```VBScript
     hybConnectCurve.Base Curve = 1

```

### Property **FirstContinuity**( ) As long

   Gets or Sets the continuity on first curve. FirstContinuity = 0 : Point continuity = 1 : Tangency continuity = 2 : Curvature continuity  
### Property **FirstCurve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets or Sets the first reference curve. new first reference curve  
### Property **FirstOrientation**( ) As long

   Gets or Sets the orientation of first curve FirstOrientation = 1 : SameOrientation. = -1 : InvertOrientation. = 2 : KoOrientation  
### Property **FirstPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets or Sets the first reference point. new first reference point  
### Property **FirstTension**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the tension on the first curve making up the connect curve.

**Example:**      This example retrieves the tension of the first curve that makes up the connect curve `hybConnect`.

```VBScript
     Dim firstCurveTension As CATIARealParam
     firstCurveTension = hybConnect.FirstTension

```

### Property **SecondContinuity**( ) As long

   Gets or Sets the continuity on second curve. SecondContinuity = 0 : Point continuity = 1 : Tangency continuity = 2 : Curvature continuity  
### Property **SecondCurve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets or Sets the second reference curve. new second reference curve  
### Property **SecondOrientation**( ) As long

   Gets or Sets the orientation of second curve SecondOrientation = 1 : SameOrientation. = -1 : InvertOrientation. = 2 : KoOrientation  
### Property **SecondPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets or Sets the second reference point. new second reference point  
### Property **SecondTension**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the tension on the second curve making up the connect curve.

**Example:**      This example retrieves the tension of the second curve that makes up the connect curve `hybConnect`.

```VBScript
     Dim secondCurveTension As CATIARealParam
     secondCurveTension = hybConnect.SecondTension

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the supporting face.

**Do not use this property** 
### Property **Trim**( ) As boolean

   Gets or Sets the trim mode. Trim = FALSE : Connected curves are not trimmed. = TRUE : Connected curves are trimmed.