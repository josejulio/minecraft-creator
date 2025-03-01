---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.ItemCooldownComponent Class
description: Contents of the @minecraft/server.ItemCooldownComponent class.
monikerRange: "=minecraft-bedrock-experimental"
---
# ItemCooldownComponent Class

> [!CAUTION]
> This class is still in pre-release.  Its signature may change or it may be removed in future releases.

## Extends
- [*ItemComponent*](ItemComponent.md)

When present on an item, this item has a cooldown effect when used by entities.

## Properties

### **cooldownCategory**
`read-only cooldownCategory: string;`

Represents the cooldown category that this item is associated with.

Type: *string*

> [!WARNING]
> This property can throw errors when used.

### **cooldownTicks**
`read-only cooldownTicks: number;`

Amount of time, in ticks, that remain for this item cooldown.

Type: *number*

> [!WARNING]
> This property can throw errors when used.

## Methods
- [startCooldown](#startcooldown)

### **startCooldown**
`
startCooldown(player: Player): void
`

Starts a new cooldown period for this item.

#### **Parameters**
- **player**: [*Player*](Player.md)

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

## Constants

### **componentId**
`static read-only componentId = "minecraft:cooldown";`

Type: *string*
