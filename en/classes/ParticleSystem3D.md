## `ParticleSystem3D` Class

Extends [`RenderComponent`](RenderComponent.md)


Module: [cc.primitive](../modules/cc.primitive.md)
Parent Module: [cc](../modules/cc.md)


The ParticleSystem3D Component.



### Index

##### Properties

  - [`duration`](#duration) `Number` The run time of particle.
  - [`capacity`](#capacity) `Number` The maximum number of particles that a particle system can generate.
  - [`loop`](#loop) `Boolean` Whether the particle system loops.
  - [`playOnAwake`](#playonawake) `Boolean` Whether the particles start playing automatically after loaded.
  - [`prewarm`](#prewarm) `Boolean` When selected, the particle system will start playing after one round has been played (only effective when loop is enabled).
  - [`simulationSpace`](#simulationspace) `Space` The coordinate system in which the particle system is located.<br>...
  - [`simulationSpeed`](#simulationspeed) `Number` Controlling the update speed of the entire particle system.
  - [`startDelay`](#startdelay) `CurveRange` Delay particle emission time after particle system starts running.
  - [`startLifetime`](#startlifetime) `CurveRange` Particle life cycle。
  - [`startColor`](#startcolor) `GradientRange` Particle initial color
  - [`scaleSpace`](#scalespace) `Space` Particle scale space
  - [`startSize`](#startsize) `CurveRange` Initial particle size
  - [`startSpeed`](#startspeed) `CurveRange` Initial particle speed
  - [`startRotation`](#startrotation) `CurveRange` Particle initial rotation angle
  - [`gravityModifier`](#gravitymodifier) `CurveRange` Gravity coefficient of particles affected by gravity
  - [`rateOverTime`](#rateovertime) `CurveRange` Particles emitted per second
  - [`rateOverDistance`](#rateoverdistance) `CurveRange` Number of particles emitted per unit distance moved
  - [`bursts`](#bursts) `[Burst]` The number of Brusts that emit a specified number of particles at a specified time
  - [`shapeModule`](#shapemodule) `ShapeModule` Particle emitter module
  - [`colorOverLifetimeModule`](#coloroverlifetimemodule) `ColorOverLifetimeModule` Color control module
  - [`sizeOvertimeModule`](#sizeovertimemodule) `SizeOvertimeModule` Particle size module
  - [`velocityOvertimeModule`](#velocityovertimemodule) `VelocityOvertimeModule` Particle speed module
  - [`forceOvertimeModule`](#forceovertimemodule) `ForceOvertimeModule` Particle acceleration module
  - [`limitVelocityOvertimeModule`](#limitvelocityovertimemodule) `LimitVelocityOvertimeModule` Particle limit speed module (only CPU particles are supported)
  - [`rotationOvertimeModule`](#rotationovertimemodule) `RotationOvertimeModule` Particle rotation module
  - [`textureAnimationModule`](#textureanimationmodule) `TextureAnimationModule` Texture Animation Module
  - [`trailModule`](#trailmodule) `TrailModule` Particle Trajectory Module
  - [`renderMode`](#rendermode) `RenderMode` Particle generation mode
  - [`velocityScale`](#velocityscale) `Number` When the particle generation mode is StrecthedBillboard, in the direction of movement of the particles is stretched by velocity magnitude
  - [`lengthScale`](#lengthscale) `Number` When the particle generation method is StrecthedBillboard, the particles are stretched according to the particle size in the direction of motion
  - [`mesh`](#mesh) `Mesh` Particle model
  - [`particleMaterial`](#particlematerial) `Material` Particle material
  - [`trailMaterial`](#trailmaterial) `Material` Particle trail material
  - [`sharedMaterials`](#sharedmaterials) `[Material]` The materials used by this render component.
  - [`__eventTargets`](#eventtargets) `Array` Register all related EventTargets,...
  - [`node`](#node) `Node` The node this component is attached to.
  - [`uuid`](#uuid) `String` The uuid for editor.
  - [`_enabled`](#enabled) `Boolean` 
  - [`enabled`](#enabled) `Boolean` indicates whether this component is enabled or not.
  - [`enabledInHierarchy`](#enabledinhierarchy) `Boolean` indicates whether this component is enabled and its node is also active in the hierarchy.
  - [`_isOnLoadCalled`](#isonloadcalled) `Number` Returns a value which used to indicate the onLoad get called or not.
  - [`_name`](#name) `String` 
  - [`_objFlags`](#objflags) `Number` 
  - [`name`](#name) `String` The name of the object.
  - [`isValid`](#isvalid) `Boolean` Indicates whether the object is not yet destroyed.



##### Methods

  - [`play`](#play) Playing particle effects
  - [`pause`](#pause) Pause particle effect
  - [`stop`](#stop) Stop particle effect
  - [`clear`](#clear) Remove all particle effect
  - [`getMaterial`](#getmaterial) Get the material by index.
  - [`getMaterials`](#getmaterials) Gets all the materials.
  - [`setMaterial`](#setmaterial) Set the material by index.
  - [`update`](#update) This is a lifecycle method.
  - [`lateUpdate`](#lateupdate) This is a lifecycle method.
  - [`__preload`](#preload) `__preload` is called before every onLoad.
  - [`onLoad`](#onload) When attaching to an active node or its node first activated.
  - [`start`](#start) Called before all scripts' update if the Component is enabled the first time.
  - [`onEnable`](#onenable) This is a lifecycle method.
  - [`onDisable`](#ondisable) This is a lifecycle method.
  - [`onDestroy`](#ondestroy) This is a lifecycle method.
  - [`onFocusInEditor`](#onfocusineditor) 
  - [`onLostFocusInEditor`](#onlostfocusineditor) 
  - [`resetInEditor`](#resetineditor) Called to initialize the component or node’s properties when adding the component the first time or when the Reset command is used.
  - [`addComponent`](#addcomponent) Adds a component class to the node.
  - [`getComponent`](#getcomponent) Returns the component of supplied type if the node has one attached, null if it doesn't....
  - [`getComponents`](#getcomponents) Returns all components of supplied Type in the node.
  - [`getComponentInChildren`](#getcomponentinchildren) Returns the component of supplied type in any of its children using depth first search.
  - [`getComponentsInChildren`](#getcomponentsinchildren) Returns the components of supplied type in self or any of its children using depth first search.
  - [`_getLocalBounds`](#getlocalbounds) If the component's bounding box is different from the node's, you can implement this method to supply
  - [`onRestore`](#onrestore) for undo/redo operation.
  - [`schedule`](#schedule) Schedules a custom selector....
  - [`scheduleOnce`](#scheduleonce) Schedules a callback function that runs only once, with a delay of 0 or larger.
  - [`unschedule`](#unschedule) Unschedules a custom callback function.
  - [`unscheduleAllCallbacks`](#unscheduleallcallbacks) unschedule all scheduled callback functions: custom callback functions, and the 'update' callback function....
  - [`destroy`](#destroy) Actual object destruction will delayed until before rendering.
  - [`_destruct`](#destruct) Clear all references in the instance.
  - [`_onPreDestroy`](#onpredestroy) Called before the object being destroyed.
  - [`_serialize`](#serialize) The customized serialization for this object.
  - [`_deserialize`](#deserialize) Init this object from the custom serialized data.



### Details


#### Properties


##### duration

> The run time of particle.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:64](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L64) |



##### capacity

> The maximum number of particles that a particle system can generate.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:74](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L74) |



##### loop

> Whether the particle system loops.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:91](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L91) |



##### playOnAwake

> Whether the particles start playing automatically after loaded.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:99](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L99) |



##### prewarm

> When selected, the particle system will start playing after one round has been played (only effective when loop is enabled).

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:109](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L109) |



##### simulationSpace

> The coordinate system in which the particle system is located.<br>
World coordinates (does not change when the position of other objects changes)<br>
Local coordinates (moving as the position of the parent node changes)<br>
Custom coordinates (moving with the position of a custom node)

| meta | description |
|------|-------------|
| Type | Space |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:128](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L128) |



##### simulationSpeed

> Controlling the update speed of the entire particle system.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:154](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L154) |



##### startDelay

> Delay particle emission time after particle system starts running.

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:162](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L162) |



##### startLifetime

> Particle life cycle。

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:172](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L172) |



##### startColor

> Particle initial color

| meta | description |
|------|-------------|
| Type | GradientRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:182](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L182) |



##### scaleSpace

> Particle scale space

| meta | description |
|------|-------------|
| Type | Space |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:192](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L192) |



##### startSize

> Initial particle size

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:202](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L202) |



##### startSpeed

> Initial particle speed

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:212](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L212) |



##### startRotation

> Particle initial rotation angle

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:223](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L223) |



##### gravityModifier

> Gravity coefficient of particles affected by gravity

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:235](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L235) |



##### rateOverTime

> Particles emitted per second

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:247](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L247) |



##### rateOverDistance

> Number of particles emitted per unit distance moved

| meta | description |
|------|-------------|
| Type | CurveRange |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:257](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L257) |



##### bursts

> The number of Brusts that emit a specified number of particles at a specified time

| meta | description |
|------|-------------|
| Type | Burst |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:267](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L267) |



##### shapeModule

> Particle emitter module

| meta | description |
|------|-------------|
| Type | ShapeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:294](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L294) |



##### colorOverLifetimeModule

> Color control module

| meta | description |
|------|-------------|
| Type | ColorOverLifetimeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:305](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L305) |



##### sizeOvertimeModule

> Particle size module

| meta | description |
|------|-------------|
| Type | SizeOvertimeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:316](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L316) |



##### velocityOvertimeModule

> Particle speed module

| meta | description |
|------|-------------|
| Type | VelocityOvertimeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:326](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L326) |



##### forceOvertimeModule

> Particle acceleration module

| meta | description |
|------|-------------|
| Type | ForceOvertimeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:336](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L336) |



##### limitVelocityOvertimeModule

> Particle limit speed module (only CPU particles are supported)

| meta | description |
|------|-------------|
| Type | LimitVelocityOvertimeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:346](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L346) |



##### rotationOvertimeModule

> Particle rotation module

| meta | description |
|------|-------------|
| Type | RotationOvertimeModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:356](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L356) |



##### textureAnimationModule

> Texture Animation Module

| meta | description |
|------|-------------|
| Type | TextureAnimationModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:366](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L366) |



##### trailModule

> Particle Trajectory Module

| meta | description |
|------|-------------|
| Type | TrailModule |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:376](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L376) |



##### renderMode

> Particle generation mode

| meta | description |
|------|-------------|
| Type | RenderMode |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:389](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L389) |



##### velocityScale

> When the particle generation mode is StrecthedBillboard, in the direction of movement of the particles is stretched by velocity magnitude

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:414](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L414) |



##### lengthScale

> When the particle generation method is StrecthedBillboard, the particles are stretched according to the particle size in the direction of motion

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:431](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L431) |



##### mesh

> Particle model

| meta | description |
|------|-------------|
| Type | <a href="../classes/Mesh.html" class="crosslink">Mesh</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:449](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L449) |



##### particleMaterial

> Particle material

| meta | description |
|------|-------------|
| Type | <a href="../classes/Material.html" class="crosslink">Material</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:466](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L466) |



##### trailMaterial

> Particle trail material

| meta | description |
|------|-------------|
| Type | <a href="../classes/Material.html" class="crosslink">Material</a> |
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:483](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L483) |



##### sharedMaterials

> The materials used by this render component.

| meta | description |
|------|-------------|
| Type | <a href="../classes/Material.html" class="crosslink">[Material]</a> |
| Defined in | [cocos2d/core/components/CCRenderComponent.js:60](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCRenderComponent.js#L60) |



##### __eventTargets

> Register all related EventTargets,
all event callbacks will be removed in _onPreDestroy

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array" class="crosslink external" target="_blank">Array</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:61](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L61) |



##### node

> The node this component is attached to. A component is always attached to a node.

| meta | description |
|------|-------------|
| Type | <a href="../classes/Node.html" class="crosslink">Node</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:75](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L75) |

##### Examples

```js
cc.log(comp.node);
```


##### uuid

> The uuid for editor.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:106](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L106) |

##### Examples

```js
cc.log(comp.uuid);
```


##### _enabled

> 

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:147](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L147) |



##### enabled

> indicates whether this component is enabled or not.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:154](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L154) |

##### Examples

```js
comp.enabled = true;
cc.log(comp.enabled);
```


##### enabledInHierarchy

> indicates whether this component is enabled and its node is also active in the hierarchy.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:186](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L186) |

##### Examples

```js
cc.log(comp.enabledInHierarchy);
```


##### _isOnLoadCalled

> Returns a value which used to indicate the onLoad get called or not.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:202](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L202) |

##### Examples

```js
cc.log(this._isOnLoadCalled > 0);
```


##### _name

> 

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:76](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L76) |



##### _objFlags

> 

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:83](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L83) |



##### name

> The name of the object.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:240](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L240) |

##### Examples

```js
obj.name = "New Obj";
```


##### isValid

> Indicates whether the object is not yet destroyed. (It will not be available after being destroyed)<br>
When an object's `destroy` is called, it is actually destroyed after the end of this frame.
So `isValid` will return false from the next frame, while `isValid` in the current frame will still be true.
If you want to determine whether the current frame has called `destroy`, use `cc.isValid(obj, true)`,
but this is often caused by a particular logical requirements, which is not normally required.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:258](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L258) |

##### Examples

```js
var node = new cc.Node();
cc.log(node.isValid);    // true
node.destroy();
cc.log(node.isValid);    // true, still valid in this frame
// after a frame...
cc.log(node.isValid);    // false, destroyed in the end of last frame
```





<!-- Method Block -->
#### Methods


##### play

Playing particle effects

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:563](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L563) |



##### pause

Pause particle effect

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:587](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L587) |



##### stop

Stop particle effect

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:604](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L604) |



##### clear

Remove all particle effect

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/3d/particle/particle-system-3d.ts:628](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/3d/particle/particle-system-3d.ts#L628) |



##### getMaterial

Get the material by index.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/MaterialVariant.html" class="crosslink">MaterialVariant</a> 
| Defined in | [cocos2d/core/components/CCRenderComponent.js:150](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCRenderComponent.js#L150) |

###### Parameters
- `index` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> 


##### getMaterials

Gets all the materials.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/MaterialVariant.html" class="crosslink">[MaterialVariant]</a> 
| Defined in | [cocos2d/core/components/CCRenderComponent.js:173](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCRenderComponent.js#L173) |



##### setMaterial

Set the material by index.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Material.html" class="crosslink">Material</a> 
| Defined in | [cocos2d/core/components/CCRenderComponent.js:187](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCRenderComponent.js#L187) |

###### Parameters
- `index` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> 
- `material` <a href="../classes/Material.html" class="crosslink">Material</a> 


##### update

Update is called every frame, if the Component is enabled.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:223](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L223) |

###### Parameters
- `dt` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> the delta time in seconds it took to complete the last frame


##### lateUpdate

LateUpdate is called every frame, if the Component is enabled.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:234](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L234) |



##### __preload

`__preload` is called before every onLoad.
It is used to initialize the builtin components internally,
to avoid checking whether onLoad is called before every public method calls.
This method should be removed if script priority is supported.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:244](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L244) |



##### onLoad

When attaching to an active node or its node first activated.
onLoad is always called before any start functions, this allows you to order initialization of scripts.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:255](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L255) |



##### start

Called before all scripts' update if the Component is enabled the first time.
Usually used to initialize some logic which need to be called after all components' `onload` methods called.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:268](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L268) |



##### onEnable

Called when this component becomes enabled and its node is active.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:281](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L281) |



##### onDisable

Called when this component becomes disabled or its node becomes inactive.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:291](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L291) |



##### onDestroy

Called when this component will be destroyed.<br/>
This is a lifecycle method. It may not be implemented in the super class. You can only call its super class method inside it. It should not be called manually elsewhere.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:301](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L301) |



##### onFocusInEditor



| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:311](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L311) |



##### onLostFocusInEditor



| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:316](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L316) |



##### resetInEditor

Called to initialize the component or node’s properties when adding the component the first time or when the Reset command is used. This function is only called in editor.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:321](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L321) |



##### addComponent

Adds a component class to the node. You can also add component to node by passing in the name of the script.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:331](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L331) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> the constructor or the class name of the component to add

##### Examples

```js
var sprite = node.addComponent(cc.Sprite);
var test = node.addComponent("Test");
```

##### getComponent

Returns the component of supplied type if the node has one attached, null if it doesn't.<br/>
You can also get component in the node by passing in the name of the script.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:349](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L349) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
// get sprite component.
var sprite = node.getComponent(cc.Sprite);
// get custom test calss.
var test = node.getComponent("Test");
```

##### getComponents

Returns all components of supplied Type in the node.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component[]</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:373](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L373) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
var sprites = node.getComponents(cc.Sprite);
var tests = node.getComponents("Test");
```

##### getComponentInChildren

Returns the component of supplied type in any of its children using depth first search.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:391](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L391) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
var sprite = node.getComponentInChildren(cc.Sprite);
var Test = node.getComponentInChildren("Test");
```

##### getComponentsInChildren

Returns the components of supplied type in self or any of its children using depth first search.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component[]</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:409](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L409) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
var sprites = node.getComponentsInChildren(cc.Sprite);
var tests = node.getComponentsInChildren("Test");
```

##### _getLocalBounds

If the component's bounding box is different from the node's, you can implement this method to supply
a custom axis aligned bounding box (AABB), so the editor's scene view can perform hit test properly.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:429](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L429) |

###### Parameters
- `out_rect` <a href="../classes/Rect.html" class="crosslink">Rect</a> the Rect to receive the bounding box


##### onRestore

onRestore is called after the user clicks the Reset item in the Inspector's context menu or performs
an undo operation on this component.<br/>
<br/>
If the component contains the "internal state", short for "temporary member variables which not included<br/>
in its CCClass properties", then you may need to implement this function.<br/>
<br/>
The editor will call the getset accessors of your component to record/restore the component's state<br/>
for undo/redo operation. However, in extreme cases, it may not works well. Then you should implement<br/>
this function to manually synchronize your component's "internal states" with its public properties.<br/>
Once you implement this function, all the getset accessors of your component will not be called when<br/>
the user performs an undo/redo operation. Which means that only the properties with default value<br/>
will be recorded or restored by editor.<br/>
<br/>
Similarly, the editor may failed to reset your component correctly in extreme cases. Then if you need<br/>
to support the reset menu, you should manually synchronize your component's "internal states" with its<br/>
properties in this function. Once you implement this function, all the getset accessors of your component<br/>
will not be called during reset operation. Which means that only the properties with default value<br/>
will be reset by editor.

This function is only called in editor mode.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:442](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L442) |



##### schedule

Schedules a custom selector.<br/>
If the selector is already scheduled, then the interval parameter will be updated without scheduling it again.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:536](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L536) |

###### Parameters
- `callback` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">function</a> The callback function
- `interval` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> Tick interval in seconds. 0 means tick every frame.
- `repeat` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> The selector will be executed (repeat + 1) times, you can use cc.macro.REPEAT_FOREVER for tick infinitely.
- `delay` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> The amount of time that the first tick will wait before execution. Unit: s

##### Examples

```js
var timeCallback = function (dt) {
  cc.log("time: " + dt);
}
this.schedule(timeCallback, 1);
```

##### scheduleOnce

Schedules a callback function that runs only once, with a delay of 0 or larger.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:574](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L574) |

###### Parameters
- `callback` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">function</a> A function wrapped as a selector
- `delay` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> The amount of time that the first tick will wait before execution. Unit: s

##### Examples

```js
var timeCallback = function (dt) {
  cc.log("time: " + dt);
}
this.scheduleOnce(timeCallback, 2);
```

##### unschedule

Unschedules a custom callback function.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:591](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L591) |

###### Parameters
- `callback_fn` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">function</a> A function wrapped as a selector

##### Examples

```js
this.unschedule(_callback);
```

##### unscheduleAllCallbacks

unschedule all scheduled callback functions: custom callback functions, and the 'update' callback function.<br/>
Actions are not affected by this method.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:607](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/components/CCComponent.js#L607) |


##### Examples

```js
this.unscheduleAllCallbacks();
```

##### destroy

Destroy this Object, and release all its own references to other objects.<br/>
Actual object destruction will delayed until before rendering.
From the next frame, this object is not usable any more.
You can use cc.isValid(obj) to check whether the object is destroyed before accessing it.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
| Defined in | [cocos2d/core/platform/CCObject.js:293](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L293) |


##### Examples

```js
obj.destroy();
```

##### _destruct

Clear all references in the instance.

NOTE: this method will not clear the getter or setter functions which defined in the instance of CCObject.
      You can override the _destruct method if you need, for example:
      _destruct: function () {
          for (var key in this) {
              if (this.hasOwnProperty(key)) {
                  switch (typeof this[key]) {
                      case 'string':
                          this[key] = '';
                          break;
                      case 'object':
                      case 'function':
                          this[key] = null;
                          break;
              }
          }
      }

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCObject.js:427](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L427) |



##### _onPreDestroy

Called before the object being destroyed.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCObject.js:460](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L460) |



##### _serialize

The customized serialization for this object. (Editor Only)

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">object</a> 
| Defined in | [cocos2d/core/platform/CCObject.js:485](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L485) |

###### Parameters
- `exporting` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### _deserialize

Init this object from the custom serialized data.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCObject.js:495](https://github.com/cocos-creator/engine/blob/33d0b730a5a6ed8ad09bd24f16c009cf509ff90b/cocos2d/core/platform/CCObject.js#L495) |

###### Parameters
- `data` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> the serialized json data
- `ctx` _Deserializer 


