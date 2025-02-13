# IManaItem

同时加载了 `Botania` 和 `CoT` 时此类才会注册进 CrT

## 导包

```zenscript
import mods.randomtweaker.item.IManaItem;
```

## 转换

你可以对 [IItemStack](https://docs.blamejared.com/1.12/en/Vanilla/Items/IItemStack/)
类的实例使用 `isIManaItem()` 方法判断其是否为 IManaItem 类的实例, 如果是即可用 `asIManaItem()` 方法将其转换

## Getter

| Getter | 返回类型 | 描述 |
| :----- | ---- | ----- |
| mana | int | 当前 Mana 值|
| maxMana | int | 能容纳的最大 Mana |
| noExport | bool | 是否真正输出 Mana |
| hasFull | bool | 是否同时有填满 Mana 的物品 |
| hasCreative | bool | 是否同时有创造型物品 |
| creative | bool | 物品是否是创造型物品 |
| full | bool | 物品是否满魔力 |

## Methods

| Method | 返回类型 | 描述 |
| :----- | ---- | ----- |
| updateMana(mana as int) | int | 增加或减少 Mana , 返回实际增加或减少值 |
| canExportManaToPool(world as [IWorld](https://docs.blamejared.com/1.12/en/Vanilla/World/IWorld/), pos as [IBlockPos](https://docs.blamejared.com/1.12/en/Vanilla/World/IBlockPos/)) | bool | 是否输出 Mana 到魔力池 ([参数解析](function.md#canexportmanatopool)) |
| canExportManaToItem(otherStack as [IItemStack](https://docs.blamejared.com/1.12/en/Vanilla/Items/IItemStack/)) | bool | 是否输出 Mana 到使用 Mana 的物品上 ([参数解析](function.md#canexportmanatoitem)) |
| canReceiveManaFromPool(world as [IWorld](https://docs.blamejared.com/1.12/en/Vanilla/World/IWorld/), pos as [IBlockPos](https://docs.blamejared.com/1.12/en/Vanilla/World/IBlockPos/)) | bool | 是否接受来自魔力池的 Mana ([参数解析](function.md#canreceivemanafrompool)) |
| canReceiveManaFromItem(otherStack as [IItemStack](https://docs.blamejared.com/1.12/en/Vanilla/Items/IItemStack/)) | bool | 是否接受来自物品的 Mana ([参数解析](function.md#canreceivemanafromitem)) |
| getUseMana() | bool | 如果此物品是 [ManaUsingItem](ManaUsingItem.md) 类实例, 则返回能否使用魔力 |