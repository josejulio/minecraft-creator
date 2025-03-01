---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.BlockType Class
description: Contents of the @minecraft/server.BlockType class.
monikerRange: "=minecraft-bedrock-experimental"
---
# BlockType Class

> [!CAUTION]
> This class is still in pre-release.  Its signature may change or it may be removed in future releases.

The type (or template) of a block. Does not contain permutation data (state) other than the type of block it represents. This type was introduced as of version 1.17.10.21.

## Properties

### **canBeWaterlogged**
`read-only canBeWaterlogged: boolean;`

Represents whether this type of block can be waterlogged.

Type: *boolean*

### **id**
`read-only id: string;`

Block type name - for example, `minecraft:acacia_stairs`.

Type: *string*
