# StrCutback (Object)

**_Represents the cutback object._**
It is aggregated to an extremity of a member. It can be retrieved using the [StrMemberExtremity](../StructureInterfaces/interface_StrMemberExtremity_70726.md) object.

## Properties

### Property **Offset**( ) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md) (Read Only)

Returns the parameter defining the offset.  
### Property **Type**( ) As [CatStrCutbackType](../StructureInterfaces/enum_CatStrCutbackType_60664.md) (Read Only)

Returns the type of the cutback object.

**Example:**      This example retrieves the type for the `StrMember` object.

```VBScript
Type = Member.Type

```