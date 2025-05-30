# ProductStructureInterfaces Framework

## Object Index

  * [Analyze](ProductStructureInterfaces/interface_Analyze_11172.md)
  * [AssemblyConvertor](ProductStructureInterfaces/interface_AssemblyConvertor_63704.md)
  * [Product](ProductStructureInterfaces/interface_Product_11223.md)
  * [ProductDocument](ProductStructureInterfaces/interface_ProductDocument_49026.md)
  * [Products](ProductStructureInterfaces/interface_Products_14720.md)
  * [Publication](ProductStructureInterfaces/interface_Publication_26668.md)
  * [Publications](ProductStructureInterfaces/interface_Publications_31954.md)

## Enumerated Types Index

  * [CatFileType](ProductStructureInterfaces/enum_CatFileType_25424.md)
  * [CatProductSource](ProductStructureInterfaces/enum_CatProductSource_54902.md)
  * [CatRepType](ProductStructureInterfaces/enum_CatRepType_21306.md)
  * [CatWorkModeType](ProductStructureInterfaces/enum_CatWorkModeType_47260.md)

---

# CatFileType (Enumeration)

**_Possible types of Files._**

**Values:**

` catFileTypeText`      Bill of material is recorded in Text File.
` catFileTypeMotif`      Bill of material is recorded in Motif File.
` catFileTypeHTML`      Bill of material is recorded in HTML File.

---

# CatProductSource (Enumeration)

**_Possible types of product source._**

**Values:**

` catProductSourceUnknown`      The product's origin is unknown
` catProductMade`      The product is made within the company
` catProductBought`      The product is bought from outside of the company

---

# CatRepType (Enumeration)

**_Possible types of representations._**

**Values:**

` catRep3D`      The representation is a 3D type
` catRep2D`      The representation is a 2D type
` catRepText`      The representation is a Text type

---

# CatWorkModeType (Enumeration)

**_Possible types of Workmode._**

**Values:**

` DESIGN`      The representation is in Design Mode
` VISUALIZATION`      The representation is in Visualization mode
` DEFAULT`      The representation is in Default Work mode

---

# Analyze (Object)

**_Represents the analysis object associated with a product._**

## Properties

### Property **Mass**( ) As double (Read Only)

   Returns the product mass value.

**Example:**      This example retrieves `MassValue` from
the `Analyze` object associated with `myProduct`:

```VBScript
     MassValue = myProduct.Analyze.Mass

```

### Property **Volume**( ) As double (Read Only)

   Returns the product volume value.

**Example:**      This example retrieves `VolumeValue` from
the `Analyze` object associated with `myProduct`:

```VBScript
     VolumeValue = myProduct.Analyze.Volume

```

### Property **WetArea**( ) As double (Read Only)

   Returns the product wet area (outer volume).
Note: This method uses **mm3** instead of default Catia V5 unit.

**Example:**      This example retrieves `WetAreaValue` from
the `Analyze` object associated with `myProduct`:

```VBScript
     WetAreaValue = myProduct.Analyze.WetArea

```

Methods

### Sub **GetGravityCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oGravityCenterCoordinatesArray`)

   Returns the gravity center coordinates of product.

**Parameters:**

` Coordinates`      The array storing the three gravity center coordinates. This array must be previously initialized.

**Example:**      This example retrieves the gravity center coordinates in `oGravityCenterCoordinatesArray` from the `Analyze` object associated with `myProduct`:

```VBScript
     ' Coordinates array initialization
     Dim oGravityCenterCoordinatesArray ( 2 )
     ' Get value in array
     Myproduct.Analyze.GetGravityCenter oGravityCenterCoordinatesArray

```

### Sub **GetInertia**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oInertiaMatrixArray`)

   Returns the inertia matrix array of product.

**Parameters:**

` oInertiaMatrixArray`      The array storing successively the three columns of inertia matrix. This array must be previously initialized.

**Example:**      This example retrieves the inertia matrix components in `oInertiaMatrixArray` from the `Analyze` object associated with `myProduct`:

```VBScript
     ' Components array initialization
     Dim oInertiaMatrixArray ( 8 )
     ' Get value in array
     Myproduct.Analyze.GetInertia oInertiaMatrixArray
     ' oInertiaMatrixArray ( 0 ) is the Ixx component
     ' oInertiaMatrixArray ( 1 ) is the Ixy component
     ' oInertiaMatrixArray ( 2 ) is the Ixz component
     ' oInertiaMatrixArray ( 3 ) is the Iyx component
     ' oInertiaMatrixArray ( 4 ) is the Iyy component
     ' oInertiaMatrixArray ( 5 ) is the Iyz component
     ' oInertiaMatrixArray ( 6 ) is the Izx component
     ' oInertiaMatrixArray ( 7 ) is the Izy component
     ' oInertiaMatrixArray ( 8 ) is the Izz component

```

---

# AssemblyConvertor (Object)

**_Product conversion object._**
The AssemblyConvertor is the object that allows saving an assembly to a specified format. Two objects exist from now on : `BillOfMaterial`, which creates a bill of material (every sub-assembly is represented, with all the one level depth components), and `ListingReport`, which creates a listing report (shows the product structure as it appears in the graph)

## Methods

### Sub **Print**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFile`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Extracts the product's contents as a specified format. Saves it in a txt, html or xls file (depends of the object).

**Parameters:**

` iFileType`      Type of the resulting file : `TXT` (for text file), `HTML` (for html file), `XLS` (for xls file) or `MOTIF` (do not use).
` iFile`      Path of the resulting file
` iProduct`      Product that will be converted

### Sub **SetCurrentFormat**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ilistProps`)

   Defines the properties that will be used in the print method.

**Parameters:**

` ilistProps`      list of properties to display

### Sub **SetSecondaryFormat**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ilistProps`)

   Defines the secondary properties that will be used in the print method.

**Parameters:**

` ilistProps`      secondary list of properties to display

---

# Product (Object)

**_Represents the product._**
The product is the object that helps you model your real products by building a tree structure whose nodes are product objects. Each of them may contain other product objects gathered in a product collection. The terminal product objects in the tree structure have no aggregated product collection. Even if all products are located somewhere in the product tree structure, some of them can be used as reference products to create other products named components, which are instances of the reference product. For example, the left front wheel in a car can be used as reference to create the other wheels. Be careful: some properties and methods are dedicated to reference objects only, and some others are for components only. This is clearly stated for each property or method concerned.

## Properties

### Property **Analyze**( ) As [CATIAAnalyze](../ProductStructureInterfaces/interface_Analyze_11172.md) (Read Only)

   Returns the Analyze object associated to the current product.

**Example:**      This example retrieves in `EngineAnalysis` the Analyze object of the `Engine` product.

```VBScript
     Dim EngineAnalysis As Analyze
     Set EngineAnalysis = Engine.Analyze

```

### Property **Definition**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the product's definition.
`Definition` is valid for reference products only.

**Example:**      This example retrieves the definition of the `Engine` product in `EngineDef`.

```VBScript
     EngineDef = Engine.Definition

```

### Property **DescriptionInst**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the product's description for a component product.
`DescriptionInst` is valid for component products only.
The description is a comment assigned to the component product to help describe or qualify it.

**Example:**      This example sets the description for the `EngineComp` product.

```VBScript
     Desc = "This is the Engine component product description"
     EngineComp.DescriptionInst(Desc)

```

### Property **DescriptionRef**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the product's description for a reference product.
`DescriptionRef` is valid for reference products only.
The description is a comment assigned to the reference product to help describe or qualify it.

**Example:**      This example sets the description for the `Engine` product.

```VBScript
     Desc = "This is the Engine reference product description"
     Engine.DescriptionRef(Desc)

```

### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the product's move object. The move object is aggregated by the product object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves your product master shape representation according to this isometry.

**Example:**      This example retrieves the move object for the `Engine` product.

```VBScript
     Dim EngineMoveObject As Move
     Set EngineMoveObject = Engine.Move

```

### Property **Nomenclature**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the product's nomenclature.
`Nomenclature` is valid for reference products only.
According to the STEP AP203, the nomenclature is "a name by which the part is commonly known within an organization".

**Example:**      This example retrieves the nomenclature the `Engine` product in `EngineNom`.

```VBScript
     EngineNom = Engine.Nomenclature

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the collection object containing the product parameters. All the parameters that are aggregated in the different objects of the product might be accessed through that collection.

**Example:**     The following example returns in `params` the parameters of the `productRoot` product from the `productDoc` product document:

```VBScript
     Set productRoot = productDoc.Product
     Set params = productRoot.Parameters

```

### Property **PartNumber**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the product's part number.
`PartNumber` is valid for reference products only.

**Example:**      This example sets the `Engine` product's part number to `A120-253X-7`.

```VBScript
     Engine.PartNumber("A120-253X-7")

```

### Property **Position**( ) As [CATIAPosition](../InfInterfaces/interface_Position_14692.md) (Read Only)

   Returns the product's position object. The position object is the object aggregated by the product object that holds the position of the master shape representation in the space.

**Example:**      This example retrieves the position object for the `Engine` product.

```VBScript
     Dim EnginePositionObject As Position
     Set EnginePositionObject = Engine.Position

```

### Property **Products**( ) As [CATIAProducts](../ProductStructureInterfaces/interface_Products_14720.md) (Read Only)

   Returns the collection of products contained in the current product.

**Example:**      This example retrieves in `EngineChildren` the collection of products contained in the `Engine` product.

```VBScript
     Dim EngineChildren As Products
     Set EngineChildren = Engine.Products

```

### Property **Publications**( ) As [CATIAPublications](../ProductStructureInterfaces/interface_Publications_31954.md) (Read Only)

   Returns the collection of publications managed by the product.  
### Property **ReferenceProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the Reference Product of this instance.  
### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

   Returns the collection object containing the product relations. All the relations that are used to valuate the parameters of the product might be accessed thru that collection.

**Example:**     The following example returns in `rels` the relations of the `productRoot` product from the `productDoc` product document:

```VBScript
     Set productRoot = productDoc.Product
     Set rels = productRoot.Relations

```

### Property **Revision**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the product's revision number.
`Revision` is valid for reference products only.

**Example:**      This example sets the `Engine` product's revision number to `3A`.

```VBScript
     Engine.Revision("3A")

```

### Property **Source**( ) As [CatProductSource](../ProductStructureInterfaces/enum_CatProductSource_54902.md)

   Returns or sets the product's source.
`Source` is valid for reference products only.
According to the STEP AP203, the source is the "design organization's plan for obtaining the product". The source can take the values catProductMade if the product is made internally, catProductBought if it is purchased from a vendor, or catProductUnknown if its origin is not determined.

**Example:**      This example sets the source for the `Engine` product to `catProductMade`.

```VBScript
     Engine.Source(catProductMade)

```

### Property **UserRefProperties**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the collection object containing the product properties. All the user defined properties that are created in the reference product might be accessed through that collection.
Only available on reference products.

**Example:**     The following example returns in `UserProps` the properties of the `productRoot` product from the `productDoc` product document:

```VBScript
     Set productRoot = productDoc.Product
     Set UserProps = productRoot.UserRefProperties

```

Methods

### Sub **ActivateDefaultShape**( )

   Activate default shape.  
### Sub **ActivateShape**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ShapeName`)

   Activate one shape.

**Parameters:**

` ShapeName`      The name of the shape.

### Sub **AddMasterShapeRepresentation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapePathName`)

   Adds the master shape representation to the product. The master shape representation is the object that gives a geometric shape and allows the visualization of the product. It can be a CATIA V4 model, a VRML file, or any other type of document that can be displayed. In a multi representation context, the master shape representation is the most meaningful representation of the product according to the user. This is the default shape for the multi representation. **Note:** This master shape representation is optional.

**Parameters:**

` iShapePathName`      The path name where the master shape representation can be found

**Example:**      This example adds the `e:\Models\Engine.model` as the master shape representation to the `Engine` product.

```VBScript
     Engine.AddMasterShapeRepresentation("e:\Models\Engine.model")

```

### Sub **AddShapeRepresentation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapePathName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  [CatRepType](../ProductStructureInterfaces/enum_CatRepType_21306.md)  `iRepBehavior`,  boolean  `iContext`)

   Adds a representation to the product with a specific behavior. A representation is the object that gives a geometric shape and allows the visualization of the product. It can be a CATIA V4 model, a VRML file, or any other type of document that can be displayed. **Note:** The possible behavior supported are : 3D, 2D and text. The representation can also be added within a context or not. A representation on a product is optional, but many representation with different behavior (or the same) is supported

**Parameters:**

` iShapePathName`      The path name where the representation can be found
` iShapeName`      The name that is given to the representation This name is a user free choice
` iRepBehavior`      The behavior of the added representation. It can take the values catRep3D if the representation is a 3D one, catRep2D if the representation is a 2D one, or catRepText if the representation is a text one.
` iContext`      A condition to specify if the added representation can be displayed with the representation of other products.

**Example:**      This example adds the `e:\Models\Engine.model` as a 3D representation to the `Engine` product within an assembly context.

```VBScript
     Engine.AddShapeRepresentation("e:\Models\Engine.model","MyShape",catRep3D,TRUE)

```

### Sub **ApplyWorkMode**( [CatWorkModeType](../ProductStructureInterfaces/enum_CatWorkModeType_47260.md)  `newMode`)

   Applies a new working mode.

**Parameters:**

` newMode`      The new working mode.

### Func **Connections**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iConnectionsType`) As [CATIACollection](../System/interface_Collection_22150.md)

   Returns the product's constraints. The constraint collection of a product gathers the constraints this product should respect to be positioned in the space.

**Example:**      This example retrieves the constraint collection for the `Engine` product.

```VBScript
     Dim EngineConstraints As Collection
     Set EngineConstraints = Engine.Constraints

```

### Func **CreateReferenceFromName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Creates a reference from a name. A reference is an object that can stand for any geometrical object. Creating references is necessary for adding constraints between two components using Brep elements of the representations of these components.

**Parameters:**

` iLabel`      The path of the Brep element to use in the constraint. This path is passed as a character string comprising the component path from the root product to the component concerned, concatenated to the Brep element path in the product's representation. Components are separated using "/", and the product path is separated from the Brep using "/!".

**Returns:**      The created reference  **Example:**      This example creates a reference from the path of a Brep element in the `Prod2` product located below the `Root` root product. The face is located in the `Pad.1` pad and limited by the `Circle.1` circle.

```VBScript
     Dim Ref As Reference
     Ref = Prod2.CreateReferenceFromName("Root/Prod2/!Face:(Brp:(Pad.1:0(Brp:(Circle.1))):None())")

```

### Sub **DesactivateDefaultShape**( )

   Deactivate default shape.  
### Sub **DesactivateShape**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ShapeName`)

   Deactivate one shape.

**Parameters:**

` ShapeName`      The name of the shape.

### Sub **ExtractBOM**( [CatFileType](../ProductStructureInterfaces/enum_CatFileType_25424.md)  `iFileType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFile`)

   Extracts the product's contents as a bill of materials (BOM). The bill of material displays, for every sub-assembly in the product, the one level depth components and some of their properties.

**Parameters:**

` iFileType`      Set this parameter to `catFileTypeHTML` to save to the html format.
Set this parameter to `catFileTypeTXT` to save to the text format.
The `catFileTypeMotif` should not be used.
` iFile`      File where the bill of material will be saved

### Func **GetActiveShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the name of the active shape.

**Returns:**      oShapeName The name of the active shape.  
### Sub **GetAllShapesNames**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `olistshape`)

   List the name of all shapes.

**Returns:**      olistshape The list of the names The tab olistshape has to be allocated with a size given by GetNumberOfShapes.  
### Func **GetDefaultShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the default shape.

**Returns:**      oShapeName The name of the default shape.  
### Func **GetMasterShapeRepresentation**( boolean  `iLoadIfNecessary`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Retrieves the product's master shape representation.

**Parameters:**

` iLoadIfNecessary`      Parameter to set to True if the master shape representation should be loaded to determine if it exists, or to False otherwise.

**Example:**      This example retrieves in `MSRep` the `Engine` product's master shape representation.

```VBScript
     Dim MSRep As Object
     Set MSRep = Engine.GetMasterShapeRepresentation(True)

```

### Func **GetMasterShapeRepresentationPathName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the product's master shape representation pathname.

**Example:**      This example retrieves in `MSRep` the `Engine` product's master shape representation.

```VBScript
     Set MSRepPath = Engine.GetMasterShapeRepresentationPathName

```

### Func **GetNumberOfShapes**( ) As short

   Returns the number of Shapes

**Returns:**      oNbShapes The number of Shapes.  
### Func **GetShapePathName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the path name of a shape for a given shape name.

**Parameters:**

` iShapeName`      The name of the shape.

**Returns:**      oShapePathName The path name of the shape.  
### Func **GetShapeRepresentation**( boolean  `iLoadIfNecessary`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  [CatRepType](../ProductStructureInterfaces/enum_CatRepType_21306.md)  `iRepBehavior`,  boolean  `iContext`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Retrieves the product's representation with the given parameters.

**Parameters:**

` iLoadIfNecessary`      Parameter to set to True if the master shape representation should be loaded to determine if it exists, or to False otherwise.
` iShapeName`      The name of the representation of the product.
` iRepBehavior`      The behavior of the representation. It can take the values catRep3D if the representation is a 3D one, catRep2D if the representation is a 2D one, or catRepText if the representation is a text one.
` iContext`      A condition to specify if the representation is displayed with the representation of other products.

**Example:**      This example retrieves in `MSRep` the `Engine` product's 3D representation named "PART".

```VBScript
     Dim MSRep As Object
     Set MSRep = Engine.GetMasterShapeRepresentation(True,"PART",catRep3D,TRUE)

```

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns the product's applicative data which type is the given parameter. The data returned can be either a collection or a simple object.

**Parameters:**

` iApplicationType`      The type of applicative data searched.

**Example:**      This example retrieves the constraints for the `Engine` product.

```VBScript
     Dim EngineConstraints As Collection
     Set EngineConstraints = Engine.GetTechnologicalObject("Constraints")

```

### Func **HasAMasterShapeRepresentation**( ) As boolean

   Returns whether the product has a master shape representation.

**True** if the product has a master shape representation.

**Example:**      This example retrieves in `HasMSRep` whether the `Engine` product has a master shape representation.

```VBScript
     HasMSRep = Engine.HasAMasterShapeRepresentation()

```

### Func **HasShapeRepresentation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  [CatRepType](../ProductStructureInterfaces/enum_CatRepType_21306.md)  `iRepBehavior`,  boolean  `iContext`) As boolean

   Returns whether the product has a representation of the given name with a given behavior.

**True** if the product has such a representation.

**Parameters:**

` iShapeName`      The name of the representation of the product.
` iRepBehavior`      The behavior of the representation. It can take the values catRep3D if the representation is a 3D one, catRep2D if the representation is a 2D one, or catRepText if the representation is a text one.
` iContext`      A condition to specify if the representation is displayed with the representation of other products.

**Example:**      This example retrieves in `HasRep` whether the `Engine` product has a master shape representation.

```VBScript
     HasRep = Engine.HasRepresentation("PART",catRep3D,TRUE)

```

### Sub **RemoveMasterShapeRepresentation**( )

   Removes the master shape representation from the product. The master shape representation is the object that gives a geometric shape and allows the visualization of the product. It can be a CATIA V4 model, a VRML file, or any other type of document that can be displayed. In a multi representation context, the master shape representation is the most meaningful representation of the product according to the user. This is the default shape for the multi representation. **Note:** This master shape representation is optional.

**Example:**      This example removes the master shape representation of the `Engine` product.

```VBScript
     Engine.RemoveMasterShapeRepresentation()

```

### Sub **RemoveShapeRepresentation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  [CatRepType](../ProductStructureInterfaces/enum_CatRepType_21306.md)  `iRepBehavior`,  boolean  `iContext`)

   Removes a specific representation from the product. A representation is the object that gives a geometric shape and allows the visualization of the product.. It can be a CATIA V4 model, a VRML file, or any other type of document that can be displayed. **Note:** This representation is optional.

**Parameters:**

` iShapeName`      The name of the representation of the product.
` iRepBehavior`      The behavior of the representation. It can take the values catRep3D if the representation is a 3D one, catRep2D if the representation is a 2D one, or catRepText if the representation is a text one.
` iContext`      A condition to specify if the representation is displayed with the representation of other products.

**Example:**      This example removes the 3D representation named "PART" of the `Engine` product.

```VBScript
     Engine.RemoveMasterShapeRepresentation
    ("PART",catRep3D,TRUE)

```

### Sub **Update**( )

   Updates the product. This update is performed with respect to the part making the product or to the product's representation. It takes into account the components of the product at any level

**Example:**      The following example updates the root product:

```VBScript
     Dim RootProduct As Product
     Set Rootproduct = productDoc.Product
     Rootproduct.Update

```

---

# ProductDocument (Object)

**_Represents the Document object for product structures._**
When a ProductDocument is created, a root product is created whose parent is the ProductDocument object. Its default name is RootProduct, which can be overwritten thanks to the the [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property. This root product is at the top of the product tree structure contained in the document. It has no difference with the other contained products, except it has no father product in the product tree structure within the document.

## Properties

### Property **Product**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the root product.

**Example:**      This example retrieves the root product of the `MyProductDoc` ProductDocument in `RootProduct`.

```VBScript
     Dim RootProduct As Product
     Set RootProduct = MyProductDoc.Product

```

---

# Products (Collection)

**_The collection of the Product objects contained in a given Product object of a ProductDocument object._**
A Product object can aggregate one or zero Products collection.

## Methods

### Func **AddComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component and adds it to the Products collection. A component is a Product object created from another Product object used as reference.

**Parameters:**

` iReferenceProduct`      The product used as reference

**Example:**      The following example creates the `SpareWheel` component from the reference product `FrontRightWheel` and adds the component to the `ToolKits` collection.

```VBScript
     Dim SpareWheel As Product
     Set SpareWheel = ToolKits.AddComponent(FrontRightWheel)

```

### Sub **AddComponentsFromFiles**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iFilesList`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMethod`)

   Creates a component for each file. The components are added to the Products collection.

**Parameters:**

` iFilesList`      The paths of the files used to retrieve the reference or the shape of th component
` iMethod`      A string describing the expected type of the files

### Func **AddExternalComponent**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iProductDocument`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component from the root product of another ProductDocument object. This root product is used as a reference to create the component. The component is added to the Products collection.

**Parameters:**

` iProductDocument`      The product document whose root object is to be used as reference to create the component

**Example:**      The following example creates the `GearBox` component by referencing the `GearBoxDocument` and adds it to the `PowerTrains` collection.

```VBScript
     Dim GearBox As Product
     Set GearBox = PowerTrains.AddExternalComponent(GearBoxDocument)

```

### Func **AddNewComponent**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumenType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component from the root product of a new ProductDocument object. This root product is used as a reference to create the component. The component is added to the Products collection.

**Parameters:**

` iProductDocument`      The product document whose root object is to be used as reference to create the component

**Example:**      The following example creates the `GearBox` component by referencing the `GearBoxDocument` and adds it to the `PowerTrains` collection.

```VBScript
     Dim GearBox As Product
     Set GearBox = PowerTrains.AddNewComponent(GearBoxDocument, "A120-253X-7")

```

### Func **AddNewProduct**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a Product reference object. This creates a Product reference object and the associated component by specifying its type and adds it to the Products collection.

**Parameters:**

` iPartNumber`      The part number of the product to be created and added to the to the collection

**Example:**      The following example creates the `Engine` product and adds the created component to the `PowerTrains` collection.

```VBScript
     Dim Engine As Product
     Set Engine = PowerTrains.AddNewProduct(V6Engine)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Returns a product from its index in the Products collection.

**Parameters:**

` iIndex`      The index of the product to retrieve in the collection of products. This index can either be the rank of the product in the collection or the name you assign to the product. As a numerics, this index is the rank of the product in the collection. The index of the first product in the collection is 1, and the index of the last product is Count. As a string, it is the name you assigned to the product using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved product  **Example:**      The following example returns in `ThisProduct` the third product, and in `ThatProduct` the product named `Wheel` in the `CarParts` product collection.

```VBScript
     Dim ThisProduct As Product
     Set ThisProduct = CarParts.Item(3)
     Dim ThatProduct As Product
     Set ThatProduct = CarParts.Item("Wheel")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a product from the Products collection.

**Parameters:**

` iIndex`      The index of the product to remove. This index can either be the rank of the product in the collection or the name you assigned to the product. As a numerics, this index is the rank of the product in the collection. The index of the first product in the collection is 1, and the index of the last product is Count. As a string, it is the name you assigned to the product using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Example:**      The following example removes the sixth product and the product named `LeftRearDisc` from the `Brakes` product collection.

```VBScript
     Brakes.Remove(6)
     Brakes.Remove("LeftRearDisc")

```

### Func **ReplaceComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iOldComponent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilePath`,  boolean  `iMultiInstances`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component which replace the given one.

**Parameters:**

` iOldComponent`      The component which will be replaced
` iFilePath`      the document to replace with
` oNewComponent`      the component replacing iOldComponent

### Func **ReplaceProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iOldComponent`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iNewReference`,  boolean  `iMultiInstances`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component which replace the given one.

**Parameters:**

` iOldComponent`      The component which will be replaced
` iNewReference`      the reference whom the old copmponent will be reconnected
` oNewComponent`      the component replacing iOldComponent

---

# Publication (Object)

**_The interface to access a CATIAPublication._**

## Properties

### Property **Relay**( [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iPub`) (Write Only)

   Valuates a publication object with another publication object. **Role:** This method allows to valuate a publication with an intermediate one.

**Parameters:**

` iPub`      The intermediate publication object

**Example:** The following example valuates the publication object `Pub1` with the publication object `Pub2`

```VBScript
     Pub1.Relay(Pub2)

```

### Property **Valuation**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns published object. **Role:** This method gives access to the finally published object.

**Parameters:**

` oRef`      The final reference of the publication object.

**Example:** This example returns the final reference `Ref` of the publication object `Pub1`.

```VBScript
     Dim Ref As Reference
     Ref = Pub1.Valuation

```

---

# Publications (Collection)

**_The collection of the Product publications._**
A Product object can aggregate one or zero Publications collection.

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPublicName`) As [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)

   Adds a publication object to the product and returns a pointer to the publication object.

**Parameters:**

` iPublicName`      The name of the publication
` oPub`      The publication object

**Example:** The following example adds a new publication object with the name "PubName" to the product and returns the publication object `Pub1`.

```VBScript
     Dim Prod1 As Product
     Set Pub1 = Prod1.Add(PubName)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIdentifier`) As [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)

   Returns the publication object corresponding to the given publication name.

**Parameters:**

` iIdentifier`      The name of the publication
` oPub`      The publication object

**Example:** The following example returns `Pub1` publication object from the product referencing the published name `PubId`.

```VBScript
     Dim Prod1 As Product
     Set Pub1 = Prod1.Item(PubId)

```

### Sub **Remove**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIdentifier`)

   Removes a publication from the product.

**Parameters:**

` iIdentifier`      The name of the publication

**Example:** The following example removes the publication object corresponding to the name `PubId`.

```VBScript
     Dim Prod1 As Product
     Prod1.Remove(PubId)

```

### Sub **SetDirect**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIdentifier`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPointed`)

   Valuates a publication object directly with the object it publishes.

**Parameters:**

` iIdentifier`      The name of the publication
` iPointed`      The published object The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md)

**Example:** The following example valuates the publication object of product `Prod1` having the name `PubId` with the reference object `RefObject`.

```VBScript
     Dim Prod1 As Product
     Prod1.SetDirect(PubId,RefObject)

```

### Sub **SetRelay**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIdentifier`,  [CATIAPublications](../ProductStructureInterfaces/interface_Publications_31954.md)  `iRelayer`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iNameInRelay`)

   Valuates a publication object with another publication object.

**Parameters:**

` iIdentifier`      The name of the publication to be valuated
` iRelayer`      The product aggregating the valuating intermediate publication object
` iNameInRelay`      The name of the valuating publication object

**Example:** The following example valuates the publication object of product `Prod1` having the name `PubId1` with the publication object of product `Prod2` having the name `PubId2`.

```VBScript
     Dim Prod1 As Product
     Prod1.SetRelay(PubId1,Prod2,PubId2)

```