# SchAppCntrColor (Object)

**_Manage graphical representation of schematic connector._**

## Methods

### Sub **AppGetConnectorColorByType**( long  `oColor`)

Specify the connector color of this connector type.

**Parameters:**

` oColor`      Application connector color for "this" connector type. Please refer to CATColorName.h of Visualization FW.
**Example:**

```VBScript
Dim objThisIntf As SchAppCntrColor
Dim intVar1 As Integer
 ...
objThisIntf.AppGetConnectorColorByTypeintVar1

```