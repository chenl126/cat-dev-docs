# ManufacturingProgram (Object)

**_A ManufacturingProgram for a Manufacturing Document._**

## Properties

### Property **Activities**( ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md) (Read Only)

Give the List of Activities linked to a Manufacturing Program.

**Example:**     The following example returns the list of Activities `ActivitiesList` linked to the manufacturing Program `CurrentProgram`

```VBScript
Set ActivitiesList = CurrentProgram.Activities

```

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Return the Default Comment of a Manufacturing Program.

**Example:**     The following example return the comment `ProgramComment` of to the manufacturing Program `CurrentProgram`

```VBScript
Set CurrentProgram.Comment= "ProgramComment"

```

Methods

### Func **AddGotoPoint**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPointName`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

Add a Goto Point Operation to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a PTP point instruction GOTO1 to the Point wich alias is`MyPoint`

```VBScript
Set GOTO1 = firstProgram.AddGotoPoint(MyPoint)

```

### Func **AddGotoPointfromCoordinates**( double  `iX`,  double  `iY`,  double  `iZ`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

Add a Goto Point Operation to a Manufacturing Program.

```VBScript
The coordinates you give as input for this method have to be expressed into
the 'Absolute Axis System' not in the 'Machining Axis System' of the Part Operation.

```

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a PTP point instruction GOTO1 to the Point wich coordinates are`X,Y,Z`

```VBScript
Set GOTO1 = firstProgram.AddGotoPointfromCoordinates(X,Y,Z)

```

### Func **AddPPInstruction**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPPInstruction`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

Add a PP Instruction to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a PP Instruction PPWORD1 with text`PPWORD`

```VBScript
Set PPWORD1 = firstProgram.AddPPInstruction(PPWORD)

```

### Func **AddRotabl**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRotabl`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSens`,  double  `ival`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

Add a Table Head Rotation instruction to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in Program `firstProgram` a Rotabl ROTABL1 with argument`MODE` and angle`ANGLE1`

```VBScript
Set ROTABL1 = firstProgram.AddRotabl(MODE,ANGLE1)

```

### Func **AddToolChange**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolCatalog`,  short  `iNumSyntaxe`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

Add a Tool Change Operation to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in `firstProgram` a Tool Change Instruction with specified tool`MyTool` of specified type `ToolType`in specified catalog`ToolCatalog`

```VBScript
Set ToolChange1 = firstProgram.AddToolChange(MyTool,ToolType,ToolCatalog,Num)

```

### Func **AddToolChangeMultipleFeeds**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iToolCatalog`,  short  `iNumFSData`,  short  `iNumSyntaxe`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

Add a Tool Change Operation to a Manufacturing Program.

**Example:**     The following example create, inserts and sequences in `firstProgram` a Tool Change Instruction with specified tool`MyTool` of specified type `ToolType`in specified catalog`ToolCatalog`

```VBScript
Set ToolChange1 = firstProgram.AddToolChangeMultipleFeeds(MyTool,ToolType,ToolCatalog,NumFSData,Num)

```

### Func **AppendOperation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `type`,  short  `AutoSequence`) As [CATIAManufacturingOperation](../ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)

Create and Insert a Manufacturing Operation of a specified type to a Manufacturing Program.
if AutoSequence is set to 1, the new operation will be sequenced in the Program.

**Example:**     The following example creates, inserts and sequences in `firstProgram` the manufacturing operation `ManufacturingOperation` of type : `type`

```VBScript
Set ManufacturingOperation = firstProgram.AppendOperation(Type,1)

```

### Sub **CompletewithPolarStrategy**( [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)  `iListeMfgActivity`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAxeRef`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSensRotation`)

Complete a list of Operation in a Manufacturing Program in Polar Mode.

**Example:**     The following example complete in Program `firstProgram` a liste of Operation `ListeMo` with Reference Axis `A` and sens `CLW`

```VBScript
Call firstProgram.CompletewithPolarStrategy(ListeMo,A,CLW)

```

### Func **CreateMOfromReport**( [CATIAExpertReportObjects](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md)  `iReportSucceed`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMo`) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)

Create a list of Operation in a Manufacturing Program, of a specified type.

**Example:**     The following example create in Program `firstProgram` a liste of Operation `ListeMo` with type `Drilling` from a CATIAExpertReportSucceedCollection `ReportSucceed`.

```VBScript
Set ListeMO = firstProgram.CreateMOfromReport(ReportSucceed,Drilling)

```

### Func **GetNCOutputFile**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Get the output file (APT or ISO) associated to the program (if associated during computation).

### Func **GetTableCurrentAbsolutePosition**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iActivityRef`) As double

Get the current absolute position of the Machine Table.

**Example:**     The following example gets in Program `firstProgram` the current Machine Table absolute position `Angle` from the Manufacturing activity reference `iActivityRef`

```VBScript
Angle = firstProgram.GetTableCurrentAbsolutePosition(iActivityRef)

```

### Sub **InsertOperation**( [CATIAManufacturingOperation](../ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)  `iReferenceOperation`,  [CATIAManufacturingOperation](../ManufacturingInterfaces/interface_ManufacturingOperation_104658.md)  `iManufacturingOperation`)

Insert an existing Manufacturing Operation to a Manufacturing Program.

**Example:**     The following example inserts in `firstProgram` the manufacturing operation `ExistingOperation` after `ReferenceOperation`:

```VBScript
call firstProgram.InsertOperation(ReferenceOperation,ExistingOperation)

```

### Sub **MoveOperation**( [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iReferenceOperation`,  [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)  `iManufacturingOperation`)

Move an existing Manufacturing Operation to a Manufacturing Program.

**Example:**     The following example moves in `firstProgram` the manufacturing operation `MovedOperation` after the manufacturing operation`ExistingOperation`:

```VBScript
call firstProgram.MoveOperation(ExistingOperation, MovedOperation)

```

### Func **OrderAndCreateMOfromReport**( [CATIAExpertReportObjects](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md)  `iReportSucceed`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeMo`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAxeRotabl`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSensRotation`) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md)

Create a list of Operation in a Manufacturing Program, of a specified type.

**Example:**     The following example create in Program `firstProgram` a liste of Operation `ListeMo` with type `Drilling` from a CATIAExpertReportSucceedCollection `ReportSucceed` with Rotabl of Axis `A` and sens `CLW`.

```VBScript
Set ListeMO = firstProgram.OrderAndCreateMOfromReport(ReportSucceed,Drilling)

```