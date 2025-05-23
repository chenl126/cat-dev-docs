# ArrBendableString (Object)

**_The interface to access a CATIAArrBendableString

Using this prefered syntax will enable mkdoc to document your class._**

## Methods

### Func **GetNumOfSegments**(| ) As long

   Returns the cumulative number of the straight/arc segments that make up the Bendable object.

**Example:**      This example shows how to number of segments of `BendablePipe001`.

```VBScript
     Dim NumOfBendSegments
     NumOfBendSegments = BendablePipe001.GetNumOfSegments

```

### Func **GetNumOfSegmentsLocalAxis**( ) As long

   Returns the cumulative number of the straight/arc segments that make up the Bendable object.

### Sub **GetSegmentData**( long  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSegmentData`)

   Returns the data of the segment (Point Indices, Slope angle, Rotation Angle).

**Example:**      This example shows how to retrieve segment #2 of `BendablePipe001`.

```VBScript
     Dim SegmentData(14) As double
     BendablePipe001.GetSegmentData(2, SegmentData)
     where the data is returned in the Array in the following format...
     SegmentData(0)  = Starting Point of Segment (X Coord)
     SegmentData(1)  = Starting Point of Segment (Y Coord)
     SegmentData(2)  = Starting Point of Segment (Z Coord)
     SegmentData(3)  = End Point of Segment (X Coord)
     SegmentData(4)  = End Point of Segment (Y Coord)
     SegmentData(5)  = End Point of Segment (Z Coord)
     SegmentData(6)  = Bend Point of Segment (X Coord) '//Valid only if SegmentData(9) > 0
     SegmentData(7)  = Bend Point of Segment (Y Coord) '//Valid only if SegmentData(9) > 0
     SegmentData(8)  = Bend Point of Segment (Z Coord) '//Valid only if SegmentData(9) > 0
     SegmentData(9)  = Bend Radius at Bend Point '//Valid only if SegmentData(9) > 0
     SegmentData(10) = Bend Angle at Bend Point  '//Valid only if SegmentData(9) > 0
     SegmentData(11) = Rotation Angle of Segment
     SegmentData(12) = Slope Angle of Segment
     SegmentData(13) = Length of linear Segment
     SegmentData(14) = Length of Arc Segment '//Valid only if SegmentData(9) > 0

```

### Func **InstanceName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the Bendable's Instance Name.

**Example:**      This example shows how to retrieve the Bendable Instance Name of `BendablePipe001`.

```VBScript
     Dim _BendInstanceName
     _BendInstanceName = BendablePipe001.InstanceName

```