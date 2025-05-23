# PositionedMaterial (Object)

**_Represents a Positioned Material object._**

## Properties

### Property **ApplicationMode**(| ) As short (Read Only)

   Returns the application mode of the material.

Possible mode values are:
  * 0: Material has been applied as a copy on the geometrical object
  * 1: Material has been applied as a link on the geometrical object

### Property **InheritanceMode**( ) As short

   Returns or sets the inheritance mode of an applied material.

Possible inheritance mode values are:
  * 0: The material is propagated towards its children
  * 1: The material is not propagated towards its children
  * 2: The material do not accept material propagated by its father (forced mode)

### Property **Material**( ) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md) (Read Only)

   Returns the material object from the current positioned material.