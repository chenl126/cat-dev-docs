# PspApplication (Object)

**_Represents an application._**

**Role** : To activate and query a Distributive System application.

## Methods

### Sub **Initialization**(| )

   Initializes the application environment (load feature start up objects, activate the application..).

**Example:**

```VBScript
     Dim objPrdRoot        As Product
     Dim objPspWorkbench   As PspWorkbench
     Dim objPspApplnPip       As PspApplication
     Dim objPspApplnTub    As PspApplication

     Set objPrdRoot = CATIA.ActiveDocument.Product
     Set objPspWorkbench = objPrdRoot.GetTechnologicalObject ("PspWorkbench")

     Set objPspApplnPip = objPspWorkbench.GetApplication(catPspIDLCATPiping)
     ...

     objPspApplnPip.Initialization
     ....
     Set objPspApplnTub = objPspWorkbench.GetApplication(catPspIDLCATTubing)

```