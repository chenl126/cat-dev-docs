# Tracks (Collection)

**_A collection of all the track objects contained in the current document._**

## Methods

### Sub **AddFromFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`)

Creates a track in the collection, from information from an external file.

**Parameters:**

` iFileName`      The path to a valid xml file.  **Example:**      The following example reads a file called `exmple.xml` and creates a track in the tracks collection.

```VBScript
myTracks.AddFromFile ("example.xml")

```