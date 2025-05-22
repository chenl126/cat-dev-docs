# KinematicsWorkbench (Object)

**_Interface to access all Kinematics entities._**

## Properties

### Property **Mechanisms**( ) As [CATIAMechanisms](../KinematicsInterfaces/interface_Mechanisms_22166.md) (Read Only)

Returns the Mechanisms collection.

**Returns:**      The Mechanisms collection  **Example:**      This example retrieves the Mechanisms collection of the active document.

```VBScript
   Dim TheKinWorkbench As Workbench
   Set TheKinWorkbench = CATIA.ActiveDocument.GetWorkbench ( "KinematicsWorkbench" )
   Dim TheMechanismsList As Mechanisms
   Set TheMechanismsList = TheKinWorkbench.Mechanisms

```