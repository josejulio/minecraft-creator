---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.Entity Class
description: Contents of the @minecraft/server.Entity class.
---
# Entity Class

## Classes that extend Entity
- [*Player*](Player.md)

Represents the state of an entity (a mob, the player, or other moving objects like minecarts) in the world.

## Properties

### **dimension**
`read-only dimension: Dimension;`

Dimension that the entity is currently within.

Type: [*Dimension*](Dimension.md)

> [!WARNING]
> This property can throw errors when used.

::: moniker range="=minecraft-bedrock-experimental"
### **fallDistance**
`read-only fallDistance: number;`

The distance an entity has fallen. The value is reset when the entity is teleported. The value is always 1 when gliding with Elytra.

Type: *number*

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!WARNING]
> This property can throw errors when used.
::: moniker-end

### **id**
`read-only id: string;`

Unique identifier of the entity. This identifier is intended to be consistent across loads of a world instance. No meaning should be inferred from the value and structure of this unique identifier - do not parse or interpret it. This property is accessible even if [*@minecraft/server.Entity.isValid*](../../minecraft/server/Entity.md#isvalid) is false.

Type: *string*

### **isClimbing**
`read-only isClimbing: boolean;`

Whether the entity is touching a climbable block. For example, a player next to a ladder or a spider next to a stone wall.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

### **isFalling**
`read-only isFalling: boolean;`

Whether the entity has a fall distance greater than 0, or greater than 1 while gliding.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

### **isInWater**
`read-only isInWater: boolean;`

Whether any part of the entity is inside a water block.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

### **isOnGround**
`read-only isOnGround: boolean;`

Whether the entity is on top of a solid block.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

### **isSleeping**
`read-only isSleeping: boolean;`

If true, the entity is currently sleeping.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

### **isSneaking**
`isSneaking: boolean;`

Whether the entity is sneaking - that is, moving more slowly and more quietly.

Type: *boolean*
  
> [!IMPORTANT]
> This property can't be edited in read-only mode.

### **isSprinting**
`read-only isSprinting: boolean;`

Whether the entity is sprinting. For example, a player using the sprint action, an ocelot running away or a pig boosting with Carrot on a Stick.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

### **isSwimming**
`read-only isSwimming: boolean;`

Whether the entity is in the swimming state. For example, a player using the swim action or a fish in water.

Type: *boolean*

> [!WARNING]
> This property can throw errors when used.

::: moniker range="=minecraft-bedrock-experimental"
### **lifetimeState**
`read-only lifetimeState: EntityLifetimeState;`

Whether the entity reference that you have is valid or not.  For example, an entity may be unloaded if it moves into a chunk that is unloaded, but may be reactivated if the chunk it is within gets reloaded.

Type: [*EntityLifetimeState*](EntityLifetimeState.md)

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.
::: moniker-end

### **location**
`read-only location: Vector3;`

Current location of the entity.

Type: [*Vector3*](Vector3.md)

> [!WARNING]
> This property can throw errors when used.

### **nameTag**
`nameTag: string;`

Given name of the entity.

Type: *string*
  
> [!IMPORTANT]
> This property can't be edited in read-only mode.

### **scoreboardIdentity**
`read-only scoreboardIdentity?: ScoreboardIdentity;`

Returns a scoreboard identity that represents this entity.

Will remain valid when the entity is killed.

Type: [*ScoreboardIdentity*](ScoreboardIdentity.md)

::: moniker range="=minecraft-bedrock-experimental"
### **target**
`read-only target?: Entity;`

Retrieves or sets an entity that is used as the target of AI-related behaviors, like attacking. If the entity currently has no target returns undefined.

Type: [*Entity*](Entity.md)

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!WARNING]
> This property can throw errors when used.
::: moniker-end

### **typeId**
`read-only typeId: string;`

Identifier of the type of the entity - for example, 'minecraft:skeleton'. This property is accessible even if [*@minecraft/server.Entity.isValid*](../../minecraft/server/Entity.md#isvalid) is false.

Type: *string*

## Methods
- [addEffect](#addeffect)
- [addTag](#addtag)
- [applyDamage](#applydamage)
- [applyImpulse](#applyimpulse)
- [applyKnockback](#applyknockback)
- [clearDynamicProperties](#cleardynamicproperties)
- [clearVelocity](#clearvelocity)
::: moniker range="=minecraft-bedrock-experimental"
- [extinguishFire](#extinguishfire)
::: moniker-end
- [getBlockFromViewDirection](#getblockfromviewdirection)
- [getComponent](#getcomponent)
- [getComponents](#getcomponents)
- [getDynamicProperty](#getdynamicproperty)
- [getDynamicPropertyIds](#getdynamicpropertyids)
- [getDynamicPropertyTotalByteCount](#getdynamicpropertytotalbytecount)
- [getEffect](#geteffect)
- [getEffects](#geteffects)
- [getEntitiesFromViewDirection](#getentitiesfromviewdirection)
- [getHeadLocation](#getheadlocation)
- [getProperty](#getproperty)
- [getRotation](#getrotation)
- [getTags](#gettags)
- [getVelocity](#getvelocity)
- [getViewDirection](#getviewdirection)
- [hasComponent](#hascomponent)
- [hasTag](#hastag)
- [isValid](#isvalid)
- [kill](#kill)
- [matches](#matches)
::: moniker range="=minecraft-bedrock-experimental"
- [playAnimation](#playanimation)
::: moniker-end
- [remove](#remove)
- [removeEffect](#removeeffect)
- [removeTag](#removetag)
- [resetProperty](#resetproperty)
- [runCommand](#runcommand)
- [runCommandAsync](#runcommandasync)
- [setDynamicProperty](#setdynamicproperty)
::: moniker range="=minecraft-bedrock-experimental"
- [setOnFire](#setonfire)
::: moniker-end
- [setProperty](#setproperty)
- [setRotation](#setrotation)
- [teleport](#teleport)
- [triggerEvent](#triggerevent)
- [tryTeleport](#tryteleport)

### **addEffect**
`
addEffect(effectType: EffectType | string, duration: number, options?: EntityEffectOptions): void
`

Adds or updates an effect, like poison, to the entity.

#### **Parameters**
- **effectType**: [*EffectType*](EffectType.md) | *string*
  
  Type of effect to add to the entity.
- **duration**: *number*
  
  Amount of time, in ticks, for the effect to apply. There are 20 ticks per second. Use [*@minecraft/server.TicksPerSecond*](../../minecraft/server/minecraft-server.md#tickspersecond) constant to convert between ticks and seconds. The value must be within the range [0, 20000000].
- **options**?: [*EntityEffectOptions*](EntityEffectOptions.md) = `null`
  
  Additional options for the effect.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***addEffect.js***
```typescript
const villagerId = 'minecraft:villager_v2<minecraft:ageable_grow_up>';
const villagerLoc: mc.Vector3 = { x: 1, y: 2, z: 1 };
const villager = test.spawn(villagerId, villagerLoc);
const duration = 20;

villager.addEffect(EffectTypes.get('poison'), duration, { amplifier: 1 });
```
##### ***quickFoxLazyDog.ts***
```typescript
  const overworld = mc.world.getDimension("overworld");

  const fox = overworld.spawnEntity("minecraft:fox", {
    x: targetLocation.x + 1,
    y: targetLocation.y + 2,
    z: targetLocation.z + 3,
  });

  fox.addEffect("speed", 10, {
    amplifier: 2,
  });
  log("Created a fox.");

  const wolf = overworld.spawnEntity("minecraft:wolf", {
    x: targetLocation.x + 4,
    y: targetLocation.y + 2,
    z: targetLocation.z + 3,
  });
  wolf.addEffect("slowness", 10, {
    amplifier: 2,
  });
  wolf.isSneaking = true;
  log("Created a sneaking wolf.", 1);
```

### **addTag**
`
addTag(tag: string): boolean
`

Adds a specified tag to an entity.

#### **Parameters**
- **tag**: *string*
  
  Content of the tag to add. The tag must be less than 256 characters.

#### **Returns** *boolean* - Returns true if the tag was added successfully. This can fail if the tag already exists on the entity.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***tagsQuery.ts***
```typescript
  let mobs = ["creeper", "skeleton", "sheep"];

  // create some sample mob data
  for (let i = 0; i < 10; i++) {
    let mobTypeId = mobs[i % mobs.length];
    let entity = overworld.spawnEntity(mobTypeId, targetLocation);
    entity.addTag("mobparty." + mobTypeId);
  }

  let eqo: mc.EntityQueryOptions = {
    tags: ["mobparty.skeleton"],
  };

  for (let entity of overworld.getEntities(eqo)) {
    entity.kill();
  }
```

### **applyDamage**
`
applyDamage(amount: number, options?: EntityApplyDamageByProjectileOptions | EntityApplyDamageOptions): boolean
`

Applies a set of damage to an entity.

#### **Parameters**
- **amount**: *number*
  
  Amount of damage to apply.
- **options**?: [*EntityApplyDamageByProjectileOptions*](EntityApplyDamageByProjectileOptions.md) | [*EntityApplyDamageOptions*](EntityApplyDamageOptions.md) = `null`
  
  Additional options about the source of damage, which may add additional effects or spur additional behaviors on this entity.

#### **Returns** *boolean* - Whether the entity takes any damage. This can return false if the entity is invulnerable or if the damage applied is less than or equal to 0.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***applyDamageThenHeal.ts***
```typescript
  const skelly = overworld.spawnEntity("minecraft:skeleton", targetLocation);

  skelly.applyDamage(19); // skeletons have max damage of 20 so this is a near-death skeleton

  mc.system.runTimeout(() => {
    let health = skelly.getComponent("health") as mc.EntityHealthComponent;
    log("Skeleton health before heal: " + health.currentValue);
    health.resetToMaxValue();
    log("Skeleton health after heal: " + health.currentValue);
  }, 20);
```

### **applyImpulse**
`
applyImpulse(vector: Vector3): void
`

Applies impulse vector to the current velocity of the entity.

#### **Parameters**
- **vector**: [*Vector3*](Vector3.md)
  
  Impulse vector.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***applyImpulse.ts***
```typescript
  const zombie = overworld.spawnEntity("minecraft:zombie", targetLocation);

  zombie.clearVelocity();

  // throw the zombie up in the air
  zombie.applyImpulse({ x: 0, y: 0.5, z: 0 });
```

### **applyKnockback**
`
applyKnockback(directionX: number, directionZ: number, horizontalStrength: number, verticalStrength: number): void
`

Applies impulse vector to the current velocity of the entity.

#### **Parameters**
- **directionX**: *number*
  
  X direction in horizontal plane.
- **directionZ**: *number*
  
  Z direction in horizontal plane.
- **horizontalStrength**: *number*
  
  Knockback strength for the horizontal vector.
- **verticalStrength**: *number*
  
  Knockback strength for the vertical vector.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***bounceSkeletons.ts***
```typescript
  let mobs = ["creeper", "skeleton", "sheep"];

  // create some sample mob data
  for (let i = 0; i < 10; i++) {
    overworld.spawnEntity(mobs[i % mobs.length], targetLocation);
  }

  let eqo: mc.EntityQueryOptions = {
    type: "skeleton",
  };

  for (let entity of overworld.getEntities(eqo)) {
    entity.applyKnockback(0, 0, 0, 1);
  }
```

### **clearDynamicProperties**
`
clearDynamicProperties(): void
`

Clears all dynamic properties that have been set on this entity.

> [!WARNING]
> This function can throw errors.

### **clearVelocity**
`
clearVelocity(): void
`

Sets the current velocity of the Entity to zero. Note that this method may not have an impact on Players.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***applyImpulse.ts***
```typescript
  const zombie = overworld.spawnEntity("minecraft:zombie", targetLocation);

  zombie.clearVelocity();

  // throw the zombie up in the air
  zombie.applyImpulse({ x: 0, y: 0.5, z: 0 });
```

::: moniker range="=minecraft-bedrock-experimental"
### **extinguishFire**
`
extinguishFire(useEffects?: boolean): boolean
`

Extinguishes the fire if the entity is on fire. Note that you can call getComponent('minecraft:onfire') and, if present, the entity is on fire.

#### **Parameters**
- **useEffects**?: *boolean* = `null`
  
  Whether to show any visual effects connected to the extinguishing.

#### **Returns** *boolean* - Returns whether the entity was on fire.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***setOnFire.ts***
```typescript
  const skelly = overworld.spawnEntity("minecraft:skeleton", targetLocation);

  skelly.setOnFire(20, true);

  mc.system.runTimeout(() => {
    let onfire = skelly.getComponent("onfire") as mc.EntityOnFireComponent;
    log(onfire.onFireTicksRemaining + " fire ticks remaining.");

    skelly.extinguishFire(true);
    log("Never mind. Fire extinguished.");
  }, 20);
```
##### ***teleport.ts***
```typescript
  const cow = overworld.spawnEntity("minecraft:cow", targetLocation);

  mc.system.runTimeout(() => {
    cow.teleport(
      { x: targetLocation.x + 2, y: targetLocation.y + 2, z: targetLocation.z + 2 },
      {
        facingLocation: targetLocation,
      }
    );
  }, 20);
```
::: moniker-end

### **getBlockFromViewDirection**
`
getBlockFromViewDirection(options?: BlockRaycastOptions): BlockRaycastHit | undefined
`

Returns the first intersecting block from the direction that this entity is looking at.

#### **Parameters**
- **options**?: [*BlockRaycastOptions*](BlockRaycastOptions.md) = `null`
  
  Additional configuration options for the ray cast.

#### **Returns** [*BlockRaycastHit*](BlockRaycastHit.md) | *undefined* - Returns the first intersecting block from the direction that this entity is looking at.

> [!WARNING]
> This function can throw errors.

### **getComponent**
`
getComponent(componentId: T): EntityComponentTypeMap[T] | undefined
`

Gets a component (that represents additional capabilities) for an entity.

#### **Parameters**
- **componentId**: *T*
  
  The identifier of the component (e.g., 'minecraft:health'). If no namespace prefix is specified, 'minecraft:' is assumed. Available component IDs can be found as part of the [*@minecraft/server.EntityComponentTypes*](../../minecraft/server/EntityComponentTypes.md) enum.

#### **Returns** *EntityComponentTypeMap[T] | undefined* - Returns the component if it exists on the entity, otherwise undefined.

### **getComponents**
`
getComponents(): EntityComponent[]
`

Returns all components that are both present on this entity and supported by the API.

#### **Returns** [*EntityComponent*](EntityComponent.md)[] - Returns all components that are both present on this entity and supported by the API.

### **getDynamicProperty**
`
getDynamicProperty(identifier: string): boolean | number | string | Vector3 | undefined
`

Returns a property value.

#### **Parameters**
- **identifier**: *string*
  
  The property identifier.

#### **Returns** *boolean* | *number* | *string* | [*Vector3*](Vector3.md) | *undefined* - Returns the value for the property, or undefined if the property has not been set.

> [!WARNING]
> This function can throw errors.

### **getDynamicPropertyIds**
`
getDynamicPropertyIds(): string[]
`

Returns the available set of dynamic property identifiers that have been used on this entity.

#### **Returns** *string*[] - A string array of the dynamic properties set on this entity.

> [!WARNING]
> This function can throw errors.

### **getDynamicPropertyTotalByteCount**
`
getDynamicPropertyTotalByteCount(): number
`

Returns the total size, in bytes, of all the dynamic properties that are currently stored for this entity.  This can be useful for diagnosing performance warning signs - if, for example, an entity has many megabytes of associated dynamic properties, it may be slow to load on various devices.

#### **Returns** *number*

> [!WARNING]
> This function can throw errors.

### **getEffect**
`
getEffect(effectType: EffectType | string): Effect | undefined
`

Returns the effect for the specified EffectType on the entity, undefined if the effect is not present, or throws an error if the effect does not exist.

#### **Parameters**
- **effectType**: [*EffectType*](EffectType.md) | *string*
  
  The effect identifier.

#### **Returns** [*Effect*](Effect.md) | *undefined* - Effect object for the specified effect, undefined if the effect is not present, or throws an error if the effect does not exist.

> [!WARNING]
> This function can throw errors.

### **getEffects**
`
getEffects(): Effect[]
`

Returns a set of effects applied to this entity.

#### **Returns** [*Effect*](Effect.md)[] - List of effects.

> [!WARNING]
> This function can throw errors.

### **getEntitiesFromViewDirection**
`
getEntitiesFromViewDirection(options?: EntityRaycastOptions): EntityRaycastHit[]
`

Gets the entities that this entity is looking at by performing a ray cast from the view of this entity.

#### **Parameters**
- **options**?: [*EntityRaycastOptions*](EntityRaycastOptions.md) = `null`
  
  Additional configuration options for the ray cast.

#### **Returns** [*EntityRaycastHit*](EntityRaycastHit.md)[] - Returns a set of entities from the direction that this entity is looking at.

> [!WARNING]
> This function can throw errors.

### **getHeadLocation**
`
getHeadLocation(): Vector3
`

Returns the current location of the head component of this entity.

#### **Returns** [*Vector3*](Vector3.md) - Returns the current location of the head component of this entity.

> [!WARNING]
> This function can throw errors.

### **getProperty**
`
getProperty(identifier: string): boolean | number | string | undefined
`

Gets an entity Property value. If the property was set using the setProperty function within the same tick, the updated value will not be reflected until the subsequent tick.

#### **Parameters**
- **identifier**: *string*
  
  The entity Property identifier.

#### **Returns** *boolean* | *number* | *string* | *undefined* - Returns the current property value. For enum properties, a string is returned. For float and int properties, a number is returned. For undefined properties, undefined is returned.

> [!WARNING]
> This function can throw errors.
>
> Throws if the entity is invalid.

### **getRotation**
`
getRotation(): Vector2
`

Returns the current rotation component of this entity.

#### **Returns** [*Vector2*](Vector2.md) - Returns a Vec2 containing the rotation of this entity (in degrees).

> [!WARNING]
> This function can throw errors.

### **getTags**
`
getTags(): string[]
`

#### **Returns** *string*[] - Returns all tags associated with an entity.

> [!WARNING]
> This function can throw errors.

### **getVelocity**
`
getVelocity(): Vector3
`

Returns the current velocity vector of the entity.

#### **Returns** [*Vector3*](Vector3.md) - Returns the current velocity vector of the entity.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***getFireworkVelocity.ts***
```typescript
  const fireworkRocket = overworld.spawnEntity("minecraft:fireworks_rocket", targetLocation);

  mc.system.runTimeout(() => {
    let velocity = fireworkRocket.getVelocity();

    log("Velocity of firework is: (x: " + velocity.x + ", y:" + velocity.y + ", z:" + velocity.z + ")");
  }, 5);
```

### **getViewDirection**
`
getViewDirection(): Vector3
`

Returns the current view direction of the entity.

#### **Returns** [*Vector3*](Vector3.md) - Returns the current view direction of the entity.

> [!WARNING]
> This function can throw errors.

### **hasComponent**
`
hasComponent(componentId: string): boolean
`

Returns true if the specified component is present on this entity.

#### **Parameters**
- **componentId**: *string*
  
  The identifier of the component (e.g., 'minecraft:rideable') to retrieve. If no namespace prefix is specified, 'minecraft:' is assumed.

#### **Returns** *boolean* - Returns true if the specified component is present on this entity.

### **hasTag**
`
hasTag(tag: string): boolean
`

Returns whether an entity has a particular tag.

#### **Parameters**
- **tag**: *string*
  
  Identifier of the tag to test for.

#### **Returns** *boolean* - Returns whether an entity has a particular tag.

> [!WARNING]
> This function can throw errors.

### **isValid**
`
isValid(): boolean
`

Returns whether the entity can be manipulated by script. A Player is considered valid when it's EntityLifetimeState is set to Loaded.

#### **Returns** *boolean* - Whether the entity is valid.

### **kill**
`
kill(): boolean
`

Kills this entity. The entity will drop loot as normal.

#### **Returns** *boolean* - Returns true if entity can be killed (even if it is already dead), otherwise it returns false.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***tagsQuery.ts***
```typescript
  let mobs = ["creeper", "skeleton", "sheep"];

  // create some sample mob data
  for (let i = 0; i < 10; i++) {
    let mobTypeId = mobs[i % mobs.length];
    let entity = overworld.spawnEntity(mobTypeId, targetLocation);
    entity.addTag("mobparty." + mobTypeId);
  }

  let eqo: mc.EntityQueryOptions = {
    tags: ["mobparty.skeleton"],
  };

  for (let entity of overworld.getEntities(eqo)) {
    entity.kill();
  }
```

### **matches**
`
matches(options: EntityQueryOptions): boolean
`

Matches the entity against the passed in options. Uses the location of the entity for matching if the location is not specified in the passed in EntityQueryOptions.

#### **Parameters**
- **options**: [*EntityQueryOptions*](EntityQueryOptions.md)

#### **Returns** *boolean* - Returns true if the entity matches the criteria in the passed in EntityQueryOptions, otherwise it returns false.

> [!WARNING]
> This function can throw errors.
>
> Returns true if this entity matches the specified query criteria.

::: moniker range="=minecraft-bedrock-experimental"
### **playAnimation**
`
playAnimation(animationName: string, options?: PlayAnimationOptions): void
`

Cause the entity to play the given animation.

#### **Parameters**
- **animationName**: *string*
  
  The animation identifier. e.g. animation.creeper.swelling
- **options**?: [*PlayAnimationOptions*](PlayAnimationOptions.md) = `null`
  
  Additional options to control the playback and transitions of the animation.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.
::: moniker-end

### **remove**
`
remove(): void
`

Immediately removes the entity from the world. The removed entity will not perform a death animation or drop loot upon removal.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

### **removeEffect**
`
removeEffect(effectType: EffectType | string): boolean
`

Removes the specified EffectType on the entity, or returns false if the effect is not present.

#### **Parameters**
- **effectType**: [*EffectType*](EffectType.md) | *string*
  
  The effect identifier.

#### **Returns** *boolean* - Returns true if the effect has been removed. Returns false if the effect is not found or does not exist.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

### **removeTag**
`
removeTag(tag: string): boolean
`

Removes a specified tag from an entity.

#### **Parameters**
- **tag**: *string*
  
  Content of the tag to remove.

#### **Returns** *boolean* - Returns whether the tag existed on the entity.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

### **resetProperty**
`
resetProperty(identifier: string): boolean | number | string
`

Resets an Entity Property back to its default value, as specified in the Entity's definition. This property change is not applied until the next tick.

#### **Parameters**
- **identifier**: *string*
  
  The Entity Property identifier.

#### **Returns** *boolean* | *number* | *string* - Returns the default property value. For enum properties, a string is returned. For float and int properties, a number is returned. For undefined properties, undefined is returned.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.
>
> Throws [*@minecraft/common.EngineError*](../../minecraft/common/EngineError.md), *Error*

### **runCommand**
`
runCommand(commandString: string): CommandResult
`

Runs a synchronous command on the entity.

#### **Parameters**
- **commandString**: *string*
  
  The command string. Note: This should not include a leading forward slash.

#### **Returns** [*CommandResult*](CommandResult.md) - A command result containing whether the command was successful.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.
>
> Throws [*CommandError*](CommandError.md), *Error*

### **runCommandAsync**
`
runCommandAsync(commandString: string): Promise<CommandResult>
`

Runs a particular command asynchronously from the context of this entity. Note that there is a maximum queue of 128 asynchronous commands that can be run in a given tick.

#### **Parameters**
- **commandString**: *string*
  
  Command to run. Note that command strings should not start with slash.

#### **Returns** Promise&lt;[*CommandResult*](CommandResult.md)&gt; - For commands that return data, returns a JSON structure with command response values.

> [!WARNING]
> This function can throw errors.

### **setDynamicProperty**
`
setDynamicProperty(identifier: string, value?: boolean | number | string | Vector3): void
`

Sets a specified property to a value.

#### **Parameters**
- **identifier**: *string*
  
  The property identifier.
- **value**?: *boolean* | *number* | *string* | [*Vector3*](Vector3.md) = `null`
  
  Data value of the property to set.

> [!WARNING]
> This function can throw errors.

::: moniker range="=minecraft-bedrock-experimental"
### **setOnFire**
`
setOnFire(seconds: number, useEffects?: boolean): boolean
`

Sets an entity on fire (if it is not in water or rain). Note that you can call getComponent('minecraft:onfire') and, if present, the entity is on fire.

#### **Parameters**
- **seconds**: *number*
  
  Length of time to set the entity on fire.
- **useEffects**?: *boolean* = `null`
  
  Whether side-effects should be applied (e.g. thawing freeze) and other conditions such as rain or fire protection should be taken into consideration.

#### **Returns** *boolean* - Whether the entity was set on fire. This can fail if seconds is less than or equal to zero, the entity is wet or the entity is immune to fire.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***setOnFire.ts***
```typescript
  const skelly = overworld.spawnEntity("minecraft:skeleton", targetLocation);

  skelly.setOnFire(20, true);

  mc.system.runTimeout(() => {
    let onfire = skelly.getComponent("onfire") as mc.EntityOnFireComponent;
    log(onfire.onFireTicksRemaining + " fire ticks remaining.");

    skelly.extinguishFire(true);
    log("Never mind. Fire extinguished.");
  }, 20);
```
##### ***teleport.ts***
```typescript
  const cow = overworld.spawnEntity("minecraft:cow", targetLocation);

  mc.system.runTimeout(() => {
    cow.teleport(
      { x: targetLocation.x + 2, y: targetLocation.y + 2, z: targetLocation.z + 2 },
      {
        facingLocation: targetLocation,
      }
    );
  }, 20);
```
::: moniker-end

### **setProperty**
`
setProperty(identifier: string, value: boolean | number | string): void
`

Sets an Entity Property to the provided value. This property change is not applied until the next tick.

#### **Parameters**
- **identifier**: *string*
  
  The Entity Property identifier.
- **value**: *boolean* | *number* | *string*
  
  The property value. The provided type must be compatible with the type specified in the entity's definition. 

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.
>
> Throws if the entity is invalid.
>
> Throws if an invalid identifier is provided.
>
> Throws if the provided value type does not match the property type.
>
> Throws if the provided value is outside the expected range (int, float properties).
>
> Throws if the provided string value does not match the set of accepted enum values (enum properties

### **setRotation**
`
setRotation(rotation: Vector2): void
`

Sets the main rotation of the entity.

#### **Parameters**
- **rotation**: [*Vector2*](Vector2.md)
  
  The x and y rotation of the entity (in degrees). For most mobs, the x rotation controls the head tilt and the y rotation controls the body rotation.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

### **teleport**
`
teleport(location: Vector3, teleportOptions?: TeleportOptions): void
`

Teleports the selected entity to a new location

#### **Parameters**
- **location**: [*Vector3*](Vector3.md)
  
  New location for the entity.
- **teleportOptions**?: [*TeleportOptions*](TeleportOptions.md) = `null`
  
  Options regarding the teleport operation.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***teleportMovement.ts***
```typescript
  const pig = overworld.spawnEntity("minecraft:pig", targetLocation);

  let inc = 1;
  let runId = mc.system.runInterval(() => {
    pig.teleport(
      { x: targetLocation.x + inc / 4, y: targetLocation.y + inc / 4, z: targetLocation.z + inc / 4 },
      {
        facingLocation: targetLocation,
      }
    );

    if (inc > 100) {
      mc.system.clearRun(runId);
    }
    inc++;
  }, 4);
```

### **triggerEvent**
`
triggerEvent(eventName: string): void
`

Triggers an entity type event. For every entity, a number of events are defined in an entities' definition for key entity behaviors; for example, creepers have a minecraft:start_exploding type event.

#### **Parameters**
- **eventName**: *string*
  
  Name of the entity type event to trigger. If a namespace is not specified, minecraft: is assumed.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.
>
> If the event is not defined in the definition of the entity, an error will be thrown.

#### Examples
##### ***triggerEvent.ts***
```typescript
  const creeper = overworld.spawnEntity("minecraft:creeper", targetLocation);

  creeper.triggerEvent("minecraft:start_exploding_forced");
```

### **tryTeleport**
`
tryTeleport(location: Vector3, teleportOptions?: TeleportOptions): boolean
`

Attempts to try a teleport, but may not complete the teleport operation (for example, if there are blocks at the destination.)

#### **Parameters**
- **location**: [*Vector3*](Vector3.md)
  
  Location to teleport the entity to.
- **teleportOptions**?: [*TeleportOptions*](TeleportOptions.md) = `null`
  
  Options regarding the teleport operation.

#### **Returns** *boolean* - Returns whether the teleport succeeded. This can fail if the destination chunk is unloaded or if the teleport would result in intersecting with blocks.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.
