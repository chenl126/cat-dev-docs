# DesignTable (Object)

**_Represents the DesignTable object._**

## Properties

### Property **ColumnsNb**( ) As short (Read Only)

Returns the nb of columns in the design table file.  
### Property **Configuration**( ) As short

Returns or sets the current configuration. Legal values: 1 to ConfigurationsNb.  
### Property **ConfigurationsNb**( ) As short (Read Only)

Returns the number of design table configurations.  
### Property **CopyMode**( ) As boolean

Returns or sets whether the data contained in the file must be included inside the CATIA model.  
### Property **FilePath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the path of the design table (read/write property).  Methods

### Sub **AddAssociation**( [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iParameter`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSheetColumn`)

Adds an association between a parameter iParameter and a column of the design table. This method does nothing if the column does not exist or if the type of the parameter isn t compliant with the column type.

**Parameters:**

` iParameter`      The parameter.
` iSheetColumn`      The name of the column to be associated with the parameter.

### Sub **AddNewRow**( )

Adds a row in the design table source file. The new row is filled in with values of associated parameters. ##### Since V5R14 ##### If the file contains at least one empty row between two not empty rows, the behavior of this method is the same for Excel and Text files : => the new row containing the current parameters values replaces the first empty row found from the beginning of the file. RQ : before R14, for text files, the new row was appended at the end of the file. The empty rows were never filed by this way, so that the new row was not visible in Design Table dialog. ######################

**Returns:**      S_OK if succeeded, E_FAIL else.  
### Func **CellAsString**( short  `iRow`,  short  `iColumn`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the content of a specific cell.

**Parameters:**

` iRow`      the index of the row where the cell is located.
` iColumn`      the index of the column where the cell is located.

### Sub **RemoveAssociation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSheetColumn`)

Removes an existing association. This method does nothing if the column isn t associated or if it doesn t exist.

**Parameters:**

` iSheetColumn`      The name of an associated column.

### Sub **Synchronize**( )

Synchronizes the design table with its source file. If the file is managed in Enovia LCA, copies this file on local disk, and synchronizes design table content