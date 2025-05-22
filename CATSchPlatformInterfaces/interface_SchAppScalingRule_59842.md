# SchAppScalingRule (Object)

**_Provide application rule of how to scale schematic objects._**

## Methods

### Sub **AppGetScalingPriority**( long  `oPriority`)

Get a priority number to indicate the adjustment (moving) priority of this object during scaling.

**Parameters:**

` oPriority`      1 to 99. The lower the number, the higher the processing priority. For example, an object with priority 1 is processed first and will not move while connected objects adjust.
**Example:**

```VBScript
Dim objThisIntf As SchAppScalingRule
Dim intVar1 As Integer
 ...
objThisIntf.AppGetScalingPriorityintVar1

```