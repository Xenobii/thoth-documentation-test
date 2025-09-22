# Events

Local events are activated using the built-in method `THOTH.fire()`. This method is identical to `ATON.fire()`, provided by ATON.EventHub. Events in THOTH are built around this method.

**Syntax:**

```
THOTH.fire("eventName", args, onSuccess);
```

Photon/VRC events are activated using the built-in method `THOTH.firePhoton()`. This method is identical to `ATON.Photon.fire()`, provided by ATON.Photon. Events in THOTH are built around this method.

**Syntax:**

```
THOTH.firePhoton("eventName", args, onSuccess);
```

<!-- UI -->
## UI

Events called from the front end.

Event|Description|Arguments
:---|:---|:---
`createLayer`|Resolves layer id and calls `createLayerScene` locally and in Photon|`-`
`deleteLayer`|Calls `deleteLayerScene` locally and in Photon|`layer_id`
`ediMetadata`|Calls `editLayerScene` locally and in Photon| `layer_id`, `layer_metadata`
`selectBrush`|Selects the brush tool|`-`
`selectEraser`|Selects the eraser tool|`-`
`selectLasso`|Selects the lasso tool|`-`
`selectNone`|Deselects all tools|`-`

<!-- Scene -->
## Scene

These are events that modify the scene object Scene.currData. Usually called both locally and globally.

Event|Description|Arguments
:---|:---|:---
`createLayerScene`|Creates a new layer in scene and its respective UI element|`layer_id`
`deleteLayerScene`|Deletes a layer from the scene and its respective UI element|`layer_id`
`editLayerScene`|Edits a layer attribute|`layer_id`,`attribute`,`value`
`addToSelectionScene`|Adds faces to a layer selection|`layer_id`,`new_faces`
`delFromSelectionScene`|Removes faces from a layer selection|`layer_id`,`new_faces`

<!-- Tools -->
## Tools

Events called from the toolbox.

Event|Description|Arguments
:---|:---|:---
`useBrush`|Called to select faces with the brush tool|`-` 
`endBrush`|Called when brush selection ends to add selected faces to the active layer|`-`
`useEraser`|Called to select faces with the eraser tool|`-`
`endEraser`|Called when eraser selection ends to remove selected faces from the active layer|`-`
`startLasso`|Called to start lasso tool|`-`
`updateLasso`|Called to update the lasso during selection|`-`
`endLassoAdd`|Called when lasso selection ends to add selected faces to the active layer|`-`
`endLassoDel`|Called when lasso selection ends to remove selected faces from the active layer|`-`

<!-- Photon -->
## Photon

Events called to emit to multiple users through Photon.

Event|Description|Arguments
:---|:---|:---
`suncScene`|Emits scene state to other users|`layers` 
