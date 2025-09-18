# Events

Local events are activated using the built-in method `THOTH.fire()`. This method is identical to `ATON.fire()`, provided by ATON.EventHub. Events in THOTH are built around this method.

**Syntax:**

```
THOTH.fire("eventName", eventArguments, onSuccess);
```

Photon/VRC events are activated using the built-in method `THOTH.firePhoton()`. This method is identical to `ATON.Photon.fire()`, provided by ATON.Photon. Events in THOTH are built around this method.

**Syntax:**

```
THOTH.firePhoton("eventName", eventArguments, onSuccess);
```

## UI

### createLayer
Is called from the "New Layer" button. It fires [createLayerScene](#createlayerscene) locally and globally.

**Syntax:**

```
THOTH.fire("createLayer");
```

### deleteLayer
Is called from the "Delete Layer" button. It fires [deleteLayerScene](#deletelayerscene) locally and globally.

**Syntax:**

```
THOTH.fire("deleteLayer", id);
```


## Scene

These are events that modify the scene object Scene.currData. Usually called both locally and globally.

### createLayerScene

Called when creating a new layer from the UI. Creates a new layer and the respective UI button.

**Syntax:**

```
THOTH.fire("createLayerScene", layer_id);
THOTH.firePhoton("createLayerScene", layer_id);
```

### deleteLayerScene

Called when deleting a layer. Moves layer to trash `layer.trash = true` and hides its respective button in the UI.

**Syntax:**

```
THOTH.fire("deleteLayerScene", (id));
THOTH.firePhoton("deleteLayerScene", (id));
```

### editLayerScene

Called when editing a layer attribute.

**Syntax:**

```
l.id    = layer_id;
l.att   = attribute_to_change;
l.value = value_to_change_it_to
THOTH.fire("deleteLayerScene", l);
THOTH.firePhoton("deleteLayerScene", l);
```

### addToSelectionScene

Called when adding faces to a layer's selection.

**Syntax:**

```
l.id    = layer_id;
l.faces = faces_to_add;
THOTH.fire("addToSelectionScene", l);
THOTH.firePhoton("addToSelectionScene", l);
```

### delFromSelectionScene

Called when removing faces from a layer's selection.

**Syntax:**

```
l.id    = layer_id;
l.faces = faces_to_remove;
THOTH.fire("delFromSelectionScene", l);
THOTH.firePhoton("delFromSelectionScene", l);
```

<!---- Tools ---->
## Tools

<!-- Brush -->
### useBrush

Called while using the brush tool.

**Syntax:**

```
THOTH.fire("useBrush");
```

### endBrush

Called after using the brush tool to apply changes.

**Syntax:**

```
THOTH.fire("endBrush");
```

<!-- Eraser -->
### useEraser

Called while using the eraser tool.

**Syntax:**

```
THOTH.fire("useBrush");
```

### endEraser

Called after using the eraser tool to apply changes.

**Syntax:**

```
THOTH.fire("endEraser");
```

<!-- Lasso -->
### startLasso

Called when lasso selection starts.

**Syntax:**

```
THOTH.fire("startLasso");
```

### updateLasso

Called during lasso selection updates.

**Syntax:**

```
THOTH.fire("updateLasso");
```

### endLassoAdd

Called after lasso selection to apply changes.

**Syntax:**

```
l.id    = layer_id;
l.faces = faces_to_add;
THOTH.fire("endLassoAdd", l);
```

### endLassoDel

Called after lasso selection to apply changes.

**Syntax:**

```
l.id    = layer_id;
l.faces = faces_to_add;
THOTH.fire("endLassoDel", l);
```

<!---- Photon ---->
## Photon

<!-- syncScene -->
### syncScene

Emits scene state to other users. Fires on `"VRC_UserEnter"`.

**Syntax:**

```
layers  = THOTH.Scene.currData.layers;
THOTH.firePhoton("syncScene", layers);
```
