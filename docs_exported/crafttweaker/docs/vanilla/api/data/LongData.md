# LongData



## Importing the class

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.data.LongData;
```


## Implemented Interfaces
LongData implements the following interfaces. That means all methods defined in these interfaces are also available in LongData

- [INumberData](/vanilla/api/data/INumberData)

## Constructors

No Description Provided
```zenscript
new LongData(internal as long) as LongData
```
| Parameter | Type | Description |
|-----------|------|-------------|
| internal | long | No Description Provided |



## Casters

| Result type | Is Implicit |
|-------------|-------------|
| byte | false |
| double | false |
| float | false |
| [ICollectionData](/vanilla/api/data/ICollectionData) | false |
| int | false |
| [INumberData](/vanilla/api/data/INumberData) | false |
| long | false |
| short | false |

## Methods

:::group{name=asCollection}

Return Type: [ICollectionData](/vanilla/api/data/ICollectionData)

```zenscript
// LongData.asCollection() as ICollectionData

800000000.asCollection();
```

:::

:::group{name=asFormattedText}

Return Type: [MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
LongData.asFormattedText(indentation as string, indentDepth as int) as MCTextComponent
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
// LongData.asList() as stdlib.List<IData>

800000000.asList();
```

:::

:::group{name=asMap}

Gets a Map<String, IData> representation of this IData, returns null on anything but [MapData](/vanilla/api/data/MapData).

Returns: null if this IData is not a map.  
Return Type: [IData](/vanilla/api/data/IData)[string]

```zenscript
// LongData.asMap() as IData[string]

800000000.asMap();
```

:::

:::group{name=asNumber}

Return Type: [INumberData](/vanilla/api/data/INumberData)

```zenscript
// LongData.asNumber() as INumberData

800000000.asNumber();
```

:::

:::group{name=getByte}

Gets the value of this [IData](/vanilla/api/data/IData) as a byte

Returns: the byte value of this [IData](/vanilla/api/data/IData)  
Return Type: byte

```zenscript
// LongData.getByte() as byte

800000000.getByte();
```

:::

:::group{name=getDouble}

Gets the value of this [IData](/vanilla/api/data/IData) as a double

Returns: the double value of this [IData](/vanilla/api/data/IData)  
Return Type: double

```zenscript
// LongData.getDouble() as double

800000000.getDouble();
```

:::

:::group{name=getFloat}

Gets the value of this [IData](/vanilla/api/data/IData) as a float

Returns: the float value of this [IData](/vanilla/api/data/IData)  
Return Type: float

```zenscript
// LongData.getFloat() as float

800000000.getFloat();
```

:::

:::group{name=getId}

Gets the ID of the internal NBT tag.

 Used to determine what NBT type is stored (in a list for example)

Returns: ID of the NBT tag that this data represents.  
Return Type: byte

```zenscript
// LongData.getId() as byte

800000000.getId();
```

:::

:::group{name=getInt}

Gets the value of this [IData](/vanilla/api/data/IData) as an int

Returns: the int value of this [IData](/vanilla/api/data/IData)  
Return Type: int

```zenscript
// LongData.getInt() as int

800000000.getInt();
```

:::

:::group{name=getLong}

Gets the value of this [IData](/vanilla/api/data/IData) as a long

Returns: the long value of this [IData](/vanilla/api/data/IData)  
Return Type: long

```zenscript
// LongData.getLong() as long

800000000.getLong();
```

:::

:::group{name=getShort}

Gets the value of this [IData](/vanilla/api/data/IData) as a short

Returns: the short value of this [IData](/vanilla/api/data/IData)  
Return Type: short

```zenscript
// LongData.getShort() as short

800000000.getShort();
```

:::

:::group{name=getString}

Gets the String representation of the internal INBT tag

Returns: String that represents the internal INBT of this IData.  
Return Type: string

```zenscript
// LongData.getString() as string

800000000.getString();
```

:::


