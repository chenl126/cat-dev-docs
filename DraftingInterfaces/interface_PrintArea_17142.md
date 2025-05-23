# PrintArea (Object)

**_Manages print area of drawing sheet._**

This interface is obtained from [DrawingSheet.PrintArea](../DraftingInterfaces/interface_DrawingSheet_30816.htm#PrintArea) method.

## Properties

### Property **ActivationState**(| boolean | `iActivated`)

   Activates or deactivates the print area.

**Parameters:**

` `in`      boolean iActivated` [in] The activation state of the print area (TRUE means activated, FALSE means deactivated).

**Returns:**      Un `HRESULT`

`S_OK`      The activation state could be valuated.  `E_FAIL`      No activation or deactivation possible.  
### Property **AreaHeigth**( double  `iHeigth`)

   Valuates the heigth of the print area.

**Parameters:**

` `in`      double iHeigth` [in] The heigth of the print area. The value must be strictly positive.

**Returns:**      Un `HRESULT`

`S_OK` `E_FAIL` 
### Property **AreaLowX**( double  `iX`)

   Valuates the low x coordinate of the print area.

**Parameters:**

` `in`      double iX` [in] The low x coordinate.

**Returns:**      Un `HRESULT`

`S_OK` `E_FAIL` 
### Property **AreaLowY**( double  `iY`)

   Valuates the low y coordinate of the print area.

**Parameters:**

` `in`      double iY` [in] The low y coordinate.

**Returns:**      Un `HRESULT`

`S_OK` `E_FAIL` 
### Property **AreaWidth**( double  `iWidth`)

   Valuates the width of the print area.

**Parameters:**

` `in`      double iWidth` [in] The width of the print area. The value must be strictly positive.

**Returns:**      Un `HRESULT`

`S_OK` `E_FAIL` Methods

### Sub **GetArea**( double  `oX`,  double  `oY`,  double  `oWidth`,  double  `oHeigth`,  boolean  `oActivated`)

   Gets the printing area defined on an object. Also communicates the activation state of the printing area.  All the values are given in mm.

**Parameters:**

` `out`      double oX` [out] The low x coordinate of the area.
` `out`      double oY` [out] The low y coordinate of the area.
` `out`      double oWidth` [out] The width of the area.
` `out`      double oHeigth` [out] The heigth of the area.
` `out`      boolean oActivated` [out] The activation state of the print area (TRUE means activated, FALSE means deactivated).

**Returns:**      Un `HRESULT`

`S_OK`      The print area was succesfully retrieved.  `E_FAIL`      No print area could be retrived.  
### Sub **SetArea**( double  `iX`,  double  `iY`,  double  `iWidth`,  double  `iHeigth`)

   Sets a set of coordinates to define a rectangle print area.  All the values are given in mm.

**Parameters:**

` `in`      double iX` [in] The low x coordinate of the area.
` `in`      double iY` [in] The low y coordinate of the area.
` `in`      double iWidth` [in] The width of the area. The value must be strictly positive.
` `in`      double iHeigth` [in] The heigth of the area. The value must be strictly positive.

**Returns:**      Un `HRESULT`

`S_OK`      The print area was successfully defined.  `E_FAIL`      No print area could be defined.