# MCIngredientTransformed&LT;T : IIngredient&GT;

## 导入相关包

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.item.MCIngredientTransformed;
```


## 已实现的接口
MCIngredientTransformed implements the following interfaces. That means all methods defined in these interfaces are also available in MCIngredientTransformed

- [材料（IIngredient）](/vanilla/api/items/IIngredient)

## Casters

| 结果类型                                       | 是否隐藏 |
| ------------------------------------------ | ---- |
| [IData](/vanilla/api/data/IData)           | true |
| [MapData #地图数据](/vanilla/api/data/MapData) | true |

## 方法

:::group{name=addGlobalAttributeModifier}

Adds an AttributeModifier to this IIngredient.

 Attributes added with this method appear on all ItemStacks that match this IIngredient, regardless of how or when the ItemStack was made, if you want to have the attribute on a single specific ItemStack (such as a specific Diamond Sword made in a recipe), then you should use IItemStack#withAttributeModifier

Return Type: void

```zenscript
// MCIngredientTransformed.addGlobalAttributeModifier(attribute as Attribute, name as string, value as double, operation as AttributeOperation, slotTypes as MCEquipmentSlotType[]) as void

myMCIngredientTransformed.addGlobalAttributeModifier(<attribute:minecraft:generic.attack_damage>, "Extra Power", 10, AttributeOperation.ADDITION, [<equipmentslottype:chest>]);
```

| 参数        | 类型                                                             | 描述                                    |
| --------- | -------------------------------------------------------------- | ------------------------------------- |
| attribute | [Attribute](/vanilla/api/entity/Attribute)                     | The Attribute of the modifier.        |
| name      | string                                                         | The name of the modifier.             |
| value     | double                                                         | The value of the modifier.            |
| operation | [AttributeOperation](/vanilla/api/entity/AttributeOperation)   | The operation of the modifier.        |
| slotTypes | [MCEquipmentSlotType](/vanilla/api/util/MCEquipmentSlotType)[] | What slots the modifier is valid for. |


:::

:::group{name=addGlobalAttributeModifier}

Adds an AttributeModifier to this IIngredient using a specific UUID.

 The UUID can be used to override an existing attribute on an ItemStack with this new modifier. You can use `/ct hand attributes` to get the UUID of the attributes on an ItemStack.

 Attributes added with this method appear on all ItemStacks that match this IIngredient, regardless of how or when the ItemStack was made, if you want to have the attribute on a single specific ItemStack (such as a specific Diamond Sword made in a recipe), then you should use IItemStack#withAttributeModifier

Return Type: void

```zenscript
// MCIngredientTransformed.addGlobalAttributeModifier(attribute as Attribute, uuid as string, name as string, value as double, operation as AttributeOperation, slotTypes as MCEquipmentSlotType[]) as void

myMCIngredientTransformed.addGlobalAttributeModifier(<attribute:minecraft:generic.attack_damage>, "8c1b5535-9f79-448b-87ae-52d81480aaa3", "Extra Power", 10, AttributeOperation.ADDITION, [<equipmentslottype:chest>]);
```

| 参数        | 类型                                                             | 描述                                                |
| --------- | -------------------------------------------------------------- | ------------------------------------------------- |
| attribute | [Attribute](/vanilla/api/entity/Attribute)                     | The Attribute of the modifier.                    |
| uuid      | string                                                         | The unique identifier of the modifier to replace. |
| name      | string                                                         | The name of the modifier.                         |
| value     | double                                                         | The value of the modifier.                        |
| operation | [AttributeOperation](/vanilla/api/entity/AttributeOperation)   | The operation of the modifier.                    |
| slotTypes | [MCEquipmentSlotType](/vanilla/api/util/MCEquipmentSlotType)[] | What slots the modifier is valid for.             |


:::

:::group{name=addShiftTooltip}

Return Type: void

```zenscript
MCIngredientTransformed.addShiftTooltip(content as MCTextComponent, showMessage as MCTextComponent) as void
```

| 参数          | 类型                                                 | 描述                      | 可选    | DefaultValue |
| ----------- | -------------------------------------------------- | ----------------------- | ----- | ------------ |
| 内容          | [MCText组件](/vanilla/api/util/text/MCTextComponent) | No Description Provided | false |              |
| showMessage | [MCText组件](/vanilla/api/util/text/MCTextComponent) | No Description Provided | true  |              |


:::

:::group{name=addTooltip}

Return Type: void

```zenscript
MCIngredientTransformed.addTooltip(content as MCTextComponent) as void
```

| 参数 | 类型                                                 | 描述                      |
| -- | -------------------------------------------------- | ----------------------- |
| 内容 | [MCText组件](/vanilla/api/util/text/MCTextComponent) | No Description Provided |


:::

:::group{name=anyDamage}

Return Type: [MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
// MCIngredientTransformed.anyDamage() as MCIngredientConditioned<IIngredient>

myMCIngredientTransformed.anyDamage();
```

:::

:::group{name=clearTooltip}

Return Type: void

```zenscript
// MCIngredientTransformed.clearTooltip() as void

myMCIngredientTransformed.clearTooltip();
```

:::

:::group{name=contains}

Does the ingredient contain the given ingredient?

Return Type: boolean

```zenscript
// MCIngredientTransformed.contains(ingredient as IIngredient) as boolean

myMCIngredientTransformed.contains((<item:minecraft:iron_ingot> | <item:minecraft:gold_ingot>));
```

| 参数         | 类型                                                | 描述                      |
| ---------- | ------------------------------------------------- | ----------------------- |
| ingredient | [材料（IIngredient）](/vanilla/api/items/IIngredient) | The ingredient to check |


:::

:::group{name=matches}

Does the given stack match the ingredient?

Return Type: boolean

```zenscript
// MCIngredientTransformed.matches(stack as IItemStack) as boolean

myMCIngredientTransformed.matches(<item:minecraft:iron_ingot>);
```

| 参数    | 类型                                          | 描述                 |
| ----- | ------------------------------------------- | ------------------ |
| stack | [IItemStack](/vanilla/api/items/IItemStack) | The stack to check |


:::

:::group{name=matches}

Return Type: boolean

```zenscript
MCIngredientTransformed.matches(stack as IItemStack, ignoreDamage as boolean) as boolean
```

| 参数    | 类型                                          | 描述                      |
| ----- | ------------------------------------------- | ----------------------- |
| stack | [IItemStack](/vanilla/api/items/IItemStack) | No Description Provided |
| 忽略伤害  | boolean                                     | No Description Provided |


:::

:::group{name=modifyShiftTooltip}

Return Type: void

```zenscript
MCIngredientTransformed.modifyShiftTooltip(shiftedFunction as ITooltipFunction, unshiftedFunction as ITooltipFunction) as void
```

| 参数                | 类型                                                      | 描述                      | 可选    | DefaultValue |
| ----------------- | ------------------------------------------------------- | ----------------------- | ----- | ------------ |
| shiftedFunction   | [ITooltipFunction](/vanilla/api/items/ITooltipFunction) | No Description Provided | false |              |
| unshiftedFunction | [ITooltipFunction](/vanilla/api/items/ITooltipFunction) | No Description Provided | true  |              |


:::

:::group{name=modifyTooltip}

Return Type: void

```zenscript
MCIngredientTransformed.modifyTooltip(function as ITooltipFunction) as void
```

| 参数       | 类型                                                      | 描述                      |
| -------- | ------------------------------------------------------- | ----------------------- |
| function | [ITooltipFunction](/vanilla/api/items/ITooltipFunction) | No Description Provided |


:::

:::group{name=only}

Use this if you already have the condition from another ingredient

Return Type: [MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
MCIngredientTransformed.only(condition as IIngredientCondition<IIngredient>) as MCIngredientConditioned<IIngredient>
```

| 参数        | 类型                                                                                                                               | 描述                      |
| --------- | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| condition | [IIngredientCondition](/vanilla/api/items/IIngredientCondition)&lt;[IIngredient](/vanilla/api/items/IIngredient)&gt; | No Description Provided |


:::

:::group{name=onlyDamaged}

Return Type: [MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
// MCIngredientTransformed.onlyDamaged() as MCIngredientConditioned<IIngredient>

myMCIngredientTransformed.onlyDamaged();
```

:::

:::group{name=onlyIf}

Return Type: [MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
MCIngredientTransformed.onlyIf(uid as string, function as Predicate<IItemStack>) as MCIngredientConditioned<IIngredient>
```

| 参数       | 类型                                                                       | 描述                      | 可选    | DefaultValue |
| -------- | ------------------------------------------------------------------------ | ----------------------- | ----- | ------------ |
| uid      | string                                                                   | No Description Provided | false |              |
| function | Predicate&lt;[IItemStack](/vanilla/api/items/IItemStack)&gt; | No Description Provided | true  |              |


:::

:::group{name=removeGlobalAttribute}

Removes all AttributeModifiers that use the given Attribute from this IIngredient.

 Attributes removed with this method are removed from ItemStacks that match this IIngredient, regardless of how or when the ItemStack was made, if you want to remove the attribute on a single specific ItemStack (such as a specific Diamond Sword made in a recipe), then you should use IItemStack#withoutAttribute.

 This method can only remove default Attributes from an ItemStack, it is still possible that an ItemStack can override it.

Return Type: void

```zenscript
// MCIngredientTransformed.removeGlobalAttribute(attribute as Attribute, slotTypes as MCEquipmentSlotType[]) as void

myMCIngredientTransformed.removeGlobalAttribute(<attribute:minecraft:generic.attack_damage>, [<equipmentslottype:chest>]);
```

| 参数        | 类型                                                             | 描述                                |
| --------- | -------------------------------------------------------------- | --------------------------------- |
| attribute | [Attribute](/vanilla/api/entity/Attribute)                     | The attribute to remove.          |
| slotTypes | [MCEquipmentSlotType](/vanilla/api/util/MCEquipmentSlotType)[] | The slot types to remove it from. |


:::

:::group{name=removeGlobalAttributeModifier}

Removes all AttributeModifiers who's ID is the same as the given uuid from this IIngredient.

Return Type: void

```zenscript
// MCIngredientTransformed.removeGlobalAttributeModifier(uuid as string, slotTypes as MCEquipmentSlotType[]) as void

myMCIngredientTransformed.removeGlobalAttributeModifier("8c1b5535-9f79-448b-87ae-52d81480aaa3", [<equipmentslottype:chest>]);
```

| 参数        | 类型                                                             | 描述                                                |
| --------- | -------------------------------------------------------------- | ------------------------------------------------- |
| uuid      | string                                                         | The unique id of the AttributeModifier to remove. |
| slotTypes | [MCEquipmentSlotType](/vanilla/api/util/MCEquipmentSlotType)[] | The slot types to remove it from.                 |


:::

:::group{name=removeTooltip}

Return Type: void

```zenscript
MCIngredientTransformed.removeTooltip(regex as string) as void
```

| 参数    | 类型     | 描述                      |
| ----- | ------ | ----------------------- |
| regex | string | No Description Provided |


:::


## 运算符

:::group{name=CONTAINS}

Does the ingredient contain the given ingredient?

```zenscript
ingredient as IIngredient in myMCIngredientTransformed
(<item:minecraft:iron_ingot> | <item:minecraft:gold_ingot>) in myMCIngredientTransformed
```

:::

:::group{name=OR}

```zenscript
myMCIngredientTransformed | other as IIngredient
```

:::


## 参数

| 名称       | 类型                                                                                       | 可获得   | 可设置   | 描述                                                                               |
| -------- | ---------------------------------------------------------------------------------------- | ----- | ----- | -------------------------------------------------------------------------------- |
| 基本属性     | T                                                                                        | true  | false | No Description Provided                                                          |
| burnTime | void                                                                                     | false | true  | Sets the burn time of this ingredient, for use in the furnace and other machines |
| items    | [IItemStack](/vanilla/api/items/IItemStack)[]                                            | true  | false | No Description Provided                                                          |
| 变压器      | [IIngredientTransformer](/vanilla/api/items/IIngredientTransformer)&lt;T&gt; | true  | false | No Description Provided                                                          |
