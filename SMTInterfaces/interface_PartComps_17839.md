# PartComps (Collection)

**_Interface to access a CATIAPartComps_**

## Properties

### Property **AddedMaterialPercentage**(| ) As double (Read Only)

   Returns the added material percentage.  
### Property **AddedMaterialVolume**( ) As double (Read Only)

   Returns the added material volume.  
### Property **RemovedMaterialPercentage**( ) As double (Read Only)

   Returns the removed material percentage.  
### Property **RemovedMaterialVolume**( ) As double (Read Only)

   Returns the removed material volume.  Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct1`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct2`,  double  `iCompAccuracy`,  double  `iDispAccuracy`,  long  `iComputationType`) As [CATIAPartComp](../SMTInterfaces/interface_PartComp_13928.md)

   Computes a new comparison between products. Documents created are added to the documents in the session. Document containing the added material is called **AddedMaterial.3dmap**. Document containing the removed material is called **RemovedMaterial.3dmap**. Document containing the changed material is called **ChangedMaterial.3dmap**. If the document are meant to be kept they must be renamed, otherwise they should be deleted. Document lifecyle must be managed either with SaveAs or Close.

**Parameters:**

` iCompAccuracy`      Accuracy of the 3dmaps for the computation.
` iDispAccuracy`      Accuracy of the displayed 3dmaps.
` iComputationType`      0 : Added with position taken into account
1 : Removed with position
2 : Added + Removed with positions
3 : Added without position
4 : Removed without position
5 : Added + Removed without positions

**Returns:**      Created PartComp  **Example:**      The following example computes a comparison between two products:

```VBScript
     Dim newPartComp As PartComp
     Set newPartComp = PartComps.Add(product1, product2, 5.0, 5.0, 2)
     Dim documents1 As Documents
     Set documents1 = CATIA.Documents
     Dim document1 As Document
     Set document1 = documents1.Item("AddedMaterial.3dmap")

```