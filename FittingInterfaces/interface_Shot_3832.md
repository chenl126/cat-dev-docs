# Shot (Object)

**_The interface to access a CATIAShot._**

**Role:** A CATIAShot (or shot) is the base element that [Sampled](../FittingInterfaces/interface_Sampled_10766.md) objects are composed of. For example, when considering a [Track](../FittingInterfaces/interface_Track_5573.md), each recorded position is a shot.

## Methods

### Sub **AppendAbsDatas**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iPosition`)

   Appends to the data related to the shot. **Role:** In certain cases, a shot contains more than one data item. The SetDatas method is used to store the first data item. This method is then used to specify any additional data items

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are absolute (relative to the world coordinate system), specifically to where the object started from.

### Sub **AppendDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Appends to the data related to the shot. **Role:** In certain cases, a shot contains more than one data item. The SetDatas method is used to store the first data item. This method is then used to specify any additional data items.

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are relative to the position of object, specifically to where the object started from.

### Sub **GetAbsDatas**( short  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPosition`)

   Retrieves the data related to the shot. **Role:** To get the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory. Please note that these values are absolute (relative to the world coordinate system), specifically to where the object started from.

**Parameters:**

` iIndex`      A shot can have more than one piece of data associated to it. The value of iIndex refers to which specific data item to retrieve. The legal values of iIndex correspond to the rank of the data item (that is the 0 for the first item, 1 for the second item).

**Returns:**      An array of associated values to the shot.  
### Sub **GetDatas**( short  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPosition`)

   Retrieves the data related to the shot. **Role:** To get the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory. Please note that these values are relative to the position of object, specifically to where the object started from.

**Parameters:**

` iIndex`      A shot can have more than one piece of data associated to it. The value value of iIndex refers to which specific data item to retrieve. The legal values of iIndex correspond to the rank of the data item (that is the 0 for the first item, 1 for the second item).

**Returns:**      An array of associated values to the shot.  
### Func **GetDuration**( ) As double

   Retrieves the duration (time) associated to a shot. The duration of a shot is the amount of time needed to travel from the previous shot to the current shot. Some key things to note are:

  * The first shot should have a duration of zero.
  * The value of the duration is a positive real number. Hence, 0.454 & 1345 are legal while -18 is not.

**Returns:**      the duration of a shot.  
### Sub **GetTechnologicalDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDatas`)

   Retrieves all the data associated to the part.  
### Sub **SetAbsDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Set the data related to the shot. **Role:** To set the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory.

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are absolute (relative to the world coordinate system), specifically to where the object started from.

### Sub **SetDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Set the data related to the shot. **Role:** To set the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory.

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are relative to the position of object, specifically to where the object started from.

### Sub **SetDuration**( double  `iDuration`)

   Sets the duration (time) associated to a shot. The duration of a shot is the amount of time needed to travel from the previous shot to the current shot. Some key things to note are:

  * The first shot should have a duration of zero.
  * The value of the duration is a positive real number. Hence, 0.454 & 1345 are legal while -18 is not.

### Sub **SetTechnologicalDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDatas`)

   Sets all the data associated to the part.