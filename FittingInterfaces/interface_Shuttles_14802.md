# Shuttles (Collection)

**_The interface to access a CATIAShuttles

Using this prefered syntax will enable mkdoc to document your class._**

## Methods

### Func **Add**(| ) As [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)

   Creates a new Shuttle and adds it to the Shuttles collection.

**Returns:**      The created Shuttle  **Example:**      The following example creates a Shuttle `newShuttle` in the Shuttles collection.

```VBScript
     Set newShuttles = Shuttles.Add

```

### Func **AddFromSel**( ) As [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)

   Creates a new Shuttle from the selection and adds it to the Shuttles collection.

**Returns:**      The created Shuttle  **Example:**      The following example creates a Shuttle `newShuttle` in the Shuttles collection.

```VBScript
     Set newShuttles = Shuttles.Add

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)

### Sub **Remove**( [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)  `iShuttle`)