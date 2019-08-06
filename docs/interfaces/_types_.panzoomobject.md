> **[@panzoom/panzoom](../README.md)**

[Globals](../globals.md) / ["types"](../modules/_types_.md) / [PanzoomObject](_types_.panzoomobject.md) /

# Interface: PanzoomObject

## Hierarchy

* **PanzoomObject**

## Index

### Properties

* [getPan](_types_.panzoomobject.md#getpan)
* [getScale](_types_.panzoomobject.md#getscale)
* [options](_types_.panzoomobject.md#options)
* [pan](_types_.panzoomobject.md#pan)
* [reset](_types_.panzoomobject.md#reset)
* [setOptions](_types_.panzoomobject.md#setoptions)
* [setStyle](_types_.panzoomobject.md#setstyle)
* [zoom](_types_.panzoomobject.md#zoom)
* [zoomIn](_types_.panzoomobject.md#zoomin)
* [zoomOut](_types_.panzoomobject.md#zoomout)
* [zoomWithWheel](_types_.panzoomobject.md#zoomwithwheel)

## Properties

###  getPan

• **getPan**: *function*

*Defined in [types.ts:100](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L100)*

Get the current x/y translation

#### Type declaration:

▸ (): *object*

* **x**: *number*

* **y**: *number*

___

###  getScale

• **getScale**: *function*

*Defined in [types.ts:102](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L102)*

Get the current scale

#### Type declaration:

▸ (): *number*

___

###  options

• **options**: *[PanzoomOptions](../modules/_types_.md#panzoomoptions)*

*Defined in [types.ts:152](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L152)*

The contructed options for this Panzoom instance

___

###  pan

• **pan**: *function*

*Defined in [types.ts:113](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L113)*

Pan the Panzoom element to the given x and y coordinates

```js
// Translates the element to 50px, 100px
panzoom.pan(50, 100)
// Pans the element right 10px and down 10px from its current position
panzoom.pan(10, 10, { relative: true })
```

#### Type declaration:

▸ (`x`: number | string, `y`: number | string, `panOptions?`: [PanOptions](../modules/_types_.md#panoptions)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`x` | number \| string |
`y` | number \| string |
`panOptions?` | [PanOptions](../modules/_types_.md#panoptions) |

___

###  reset

• **reset**: *function*

*Defined in [types.ts:156](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L156)*

Reset the pan and zoom to startX, startY, and startScale

#### Type declaration:

▸ (`options?`: [PanzoomOptions](../modules/_types_.md#panzoomoptions)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`options?` | [PanzoomOptions](../modules/_types_.md#panzoomoptions) |

___

###  setOptions

• **setOptions**: *function*

*Defined in [types.ts:154](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L154)*

Change options for the Panzoom instance

#### Type declaration:

▸ (`options?`: [PanzoomOptions](../modules/_types_.md#panzoomoptions)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`options?` | [PanzoomOptions](../modules/_types_.md#panzoomoptions) |

___

###  setStyle

• **setStyle**: *[setStyle](../modules/_css_.md#setstyle)*

*Defined in [types.ts:158](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L158)*

A convenience method for setting prefixed styles on the Panzoom element

___

###  zoom

• **zoom**: *function*

*Defined in [types.ts:130](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L130)*

Zoom the Panzoom element to the given scale

```js
panzoom.zoom(2.2)
panzoom.zoom(2.2, { animate: true })
```

#### Type declaration:

▸ (`scale`: number, `zoomOptions?`: [ZoomOptions](../modules/_types_.md#zoomoptions)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`scale` | number |
`zoomOptions?` | [ZoomOptions](../modules/_types_.md#zoomoptions) |

___

###  zoomIn

• **zoomIn**: *function*

*Defined in [types.ts:117](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L117)*

Zoom in using the predetermined increment set in options

#### Type declaration:

▸ (`zoomOptions?`: [ZoomOptions](../modules/_types_.md#zoomoptions)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`zoomOptions?` | [ZoomOptions](../modules/_types_.md#zoomoptions) |

___

###  zoomOut

• **zoomOut**: *function*

*Defined in [types.ts:121](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L121)*

Zoom out using the predetermined increment set in options

#### Type declaration:

▸ (`zoomOptions?`: [ZoomOptions](../modules/_types_.md#zoomoptions)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`zoomOptions?` | [ZoomOptions](../modules/_types_.md#zoomoptions) |

___

###  zoomWithWheel

• **zoomWithWheel**: *function*

*Defined in [types.ts:150](https://github.com/timmywil/panzoom/blob/a7078e8/src/types.ts#L150)*

Zoom the Panzoom element to a focal point using the given WheelEvent

`disablePan` will prevent the focal point adjustment and will only zoom.

`zoomWithWheel` normally uses `deltaY` to determine the scale,
but will fall back to `deltaX` in case the shift modifier is used with
the wheel event. On a mac, that usually translates to horizontal scrolling,
but this method assumes the desired behavior is zooming.

This is a convenience function that may not handle all use cases.

```js
elem.parentElement.addEventListener('wheel', function(event) {
  if (!event.shiftKey) return
  panzoom.zoomUsingWheel(event)
})
```

#### Type declaration:

▸ (`event`: `WheelEvent`): *void*

**Parameters:**

Name | Type |
------ | ------ |
`event` | `WheelEvent` |