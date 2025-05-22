# KnowledgeActivateObject (Object)

**_Interface to access a CATIAKnowledgeActivableObject._**

## Properties

### Property **Activated**( ) As boolean (Read Only)

Returns whether the relation is activated.
**True** if the relation is activated. An activated relation is processed whenever the value of one of its input parameter is modified.

**Example:**      This example retrieves whether the `maximummass` relation is activated, and if true, displays the result in a message box:

```VBScript
If ( maximummass.Activated ) Then
     MsgBox "maximummass is activated"
End If

```

Methods

### Sub **Activate**( )

Activates the relation. The relation will be processed whenever the value of one of its input parameter is modified.

**Example:**      This example activates the `maximummass` relation:

```VBScript
maximummass.Activate()

```

### Sub **Deactivate**( )

Deactivates the relation. The relation will no longer be processed when the value of one of its input parameter is modified.

**Example:**      This example deactivates the `maximummass` relation:

```VBScript
maximummass.Deactivate()

```