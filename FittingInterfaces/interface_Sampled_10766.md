# Sampled (Object)

**_The interface to access a CATIASampled based object._**
The Sampled class defines characteristics for simulatable tasks within DMU Fitting. CATIASampled is the parent class for tracks. Key samples are recorded (as shots or CATIAShots) for an object and then during simulation the object is interpolated with these shots over time.

## Properties

### Property **Interpolater**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves/sets the sampled's interpolater. **Role:** Retrieves/sets the interpolator used by the sampled during simulation. Note that the name of the interpolater is used (which is a string).  
### Property **Object**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns or sets the Sampled object. **Role:/b> Retrieves/stores the object that will be used in the sampled based simulation. Please note that the object will move to the shots defined in the sampled. 
### Property **Scaling**( ) As double

   Returns or sets the Sampled object.  
### Property **Shots**( ) As [CATIAShots](../FittingInterfaces/interface_Shots_5971.md) (Read Only)

   Returns or sets the Sampled object.  
### Property **Time**( ) As double

   Retrieves/sets the sampled's time. **Role:** Retrieves/sets the internal time associated to the current sampled object. Note that the time is handled as a double.  Methods

### Func **Append**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTracks`) As [CATIASampled](../FittingInterfaces/interface_Sampled_10766.md)

   Returns or sets the Sampled object.  
### Sub **BindAnalysis**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`,  [CatSampledAnalysisMode](../FittingInterfaces/enum_CatSampledAnalysisMode_100650.md)  `iAnalysisMode`,  boolean  `iMonitorMode`)

   Add (bind) an analysis object to a Track.

**Parameters:**

` iObject`      The analysis to add (bind) to the Track
` iAnalysisMode`      Indicates the analysis status for iAnalysis CatSampledAnalysisOff CatSampledAnalysisOn, CatSampledAnalysisStop CatSampledAnalysisVerbose
` iMonitorMode`      Indicates the monitor status for iAnalysis - Off (0) or On (1)

### Sub **BreakInheritance**( )

   Returns or sets the Sampled object.  
### Sub **GetKnownInterpolaters**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oInterpolaters`)

   Returns or sets the Sampled object.  
### Func **GetTotalDuration**( ) As double

   Returns the total duration  
### Sub **RemoveAnalyses**( )

   Returns or sets the Sampled object.  
### Sub **ReverseTime**( )

   Returns or sets the Sampled object.  
### Sub **SetObjectKeepingPosition**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`)

   Sets the object in the sampled. **Role:** Stores the object that will be used in the sampled based simulation. The object will not move and the sample's shots will be repositioned relative to the object position.  
### Sub **Split**( [CatSampledSplitType](../FittingInterfaces/enum_CatSampledSplitType_76396.md)  `iType`,  short  `iIndice`)

   Returns or sets the Sampled object.