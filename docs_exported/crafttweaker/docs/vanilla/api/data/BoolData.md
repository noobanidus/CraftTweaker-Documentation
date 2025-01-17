# BoolData

Careful with BoolData: While it works for specifying boolean attributes in JSON syntax,
 using it in Tags will instead use a [ByteData](/vanilla/api/data/ByteData) object. Reason for this is that
 Minecraft does not have Boolean NBT values.

## Importing the class

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.data.BoolData;
```


## Implemented Interfaces
BoolData implements the following interfaces. That means all methods defined in these interfaces are also available in BoolData

- [IData](/vanilla/api/data/IData)

## Constructors

No Description Provided
```zenscript
new BoolData(internal as boolean) as BoolData
```
| Parameter | Type | Description |
|-----------|------|-------------|
| internal | boolean | No Description Provided |



## Casters

| Result type | Is Implicit |
|-------------|-------------|
| [ByteData](/vanilla/api/data/ByteData) | false |
| [ICollectionData](/vanilla/api/data/ICollectionData) | false |

## Methods

:::group{name=asCollection}

Return Type: [ICollectionData](/vanilla/api/data/ICollectionData)

```zenscript
// BoolData.asCollection() as ICollectionData

true.asCollection();
```

:::

:::group{name=asFormattedText}

Return Type: [MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
BoolData.asFormattedText(indentation as string, indentDepth as int) as MCTextComponent
```

| Parameter | Type | Description |
|-----------|------|-------------|
| indentation | string | No Description Provided |
| indentDepth | int | No Description Provided |


:::

:::group{name=asList}

Gets a List<IData> representation of this IData, returns null on anything but [ListData](/vanilla/api/data/ListData).

Returns: null if this IData is not a list.  
Return Type: stdlib.List&lt;[IData](/vanilla/api/data/IData)&gt;

```zenscript
// BoolData.asList() as stdlib.List<IData>

true.asList();
```

:::

:::group{name=asMap}

Gets a Map<String, IData> representation of this IData, returns null on anything but [MapData](/vanilla/api/data/MapData).

Returns: null if this IData is not a map.  
Return Type: [IData](/vanilla/api/data/IData)[string]

```zenscript
// BoolData.asMap() as IData[string]

true.asMap();
```

:::

:::group{name=contains}

Checks if this IData contains another IData, mainly used in subclasses of [ICollectionData](/vanilla/api/data/ICollectionData), is the same as an equals check on other IData types

Returns: true if the given IData is contained in this IData  
Return Type: boolean

```zenscript
// BoolData.contains(data as IData) as boolean

true.contains("Display");
```

| Parameter | Type | Description |
|-----------|------|-------------|
| data | [IData](/vanilla/api/data/IData) | data to check if it is contained |


:::

:::group{name=getByteData}

Converts this BoolData to a [ByteData](/vanilla/api/data/ByteData) object.
 This will be used when this Data is converted to NBT

Return Type: [ByteData](/vanilla/api/data/ByteData)

```zenscript
// BoolData.getByteData() as ByteData

true.getByteData();
```

:::

:::group{name=getId}

Gets the ID of the internal NBT tag.

 Used to determine what NBT type is stored (in a list for example)

Returns: ID of the NBT tag that this data represents.  
Return Type: byte

```zenscript
// BoolData.getId() as byte

true.getId();
```

:::

:::group{name=getString}

Gets the String representation of the internal INBT tag

Returns: String that represents the internal INBT of this IData.  
Return Type: string

```zenscript
// BoolData.getString() as string

true.getString();
```

:::


