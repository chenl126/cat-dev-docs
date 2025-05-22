# ManufacturingToolCorrector (Object)

**_Manufacturing tool corrector._**

## Properties

### Property **Diameter**( ) As double (Read Only)

Gives the corrector diameter tool diameter.
Returns HRESULT.

### Property **LengthNumber**( ) As short (Read Only)

Gives the corrector length number.
Returns HRESULT.

### Property **Number**( ) As short (Read Only)

Gives the corrector number.
Returns HRESULT.

### Property **Point**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Gives the corrector type point.
oPoint : Type point (Ex: P1, ..., P9)
Returns HRESULT.

### Property **RadiusNumber**( ) As short (Read Only)

Gives the corrector radius number.
Returns HRESULT.
Methods

### Sub **GetValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPoint`,  short  `oNumber`,  short  `oLengthNumber`,  short  `oRadiusNumber`,  double  `oDiameter`)

Gives the corrector values.
oPoint : Type point (Ex: P1, ..., P9)
oNumber : Corrector Number
oLengthNumber : Corrector Length Number
oRadiusNumber : Corrector Radius Number
oDiameter : Tool Diameter where corrector applyes (if non fixed corrector)
Returns HRESULT.

### Sub **SetValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPoint`,  short  `oNumber`,  short  `oLengthNumber`,  short  `oRadiusNumber`,  double  `oDiameter`)

Defines the corrector values.
iPoint : Type point (Ex: P1, ..., P9)
iNumber : Corrector Number
iLengthNumber : Corrector Length Number
iRadiusNumber : Corrector Radius Number
iDiameter : Tool Diameter where corrector applyes (if non fixed corrector)
Returns HRESULT.