# Layers

![new-layer-icon](../assets/icons/layers.png)

## Layer Overview

Each layer can be thought of as a different annotation object, in other words a structured descriptor for a specific selection. Visually, it is represented by the selected faces on the object. As an entity, it can be described by its name and metadata.

THOTH layers are objects which contain the following attributes:

Attribute|Description
:---|:---
`id`|: The uinque id assigned to the layer.
`name`| The name of the layer.
`metadata`| The metadata associated with the selection.
`selection`| The set of faces to which the metadata is assigned to.
`color`| The color the layer selection will be displayed as.
`visible`| Defines whether a layer is visible or hidden.

The user can create new layers, as well as modify and delete existing layers. This can be achieved from the layer panel accessed from the Layers button.

## Creating a new layer

From the layer panel, a new layer can be created by pressing the Create New Layer button.

![new-layer-icon](../assets/icons/add.png)

This will automatically assign an id to the new layer as well as a default name and color. 

The user can select the created layer by pressing its name on the layer panel.


## Modifying a layer

For a selected layer, the user can directly alter any of its attributes with the appropriate tools and ui elements.

* **Name**: The name of the layer can edited by double clicking the layer name in the layer panel.

* **Metadata**: The metadata can be edited by pressing the Edit Metadata button. This will show the respective modal, where the user can input values for any of the layer's properties, based on the TEXTaiLES schema.

* **Selection**: After selecting a layer, use the tools provided to mark an area on the object. The selection will automatically be assigned to the selected layer.

* **Visibility**: You can toggle the visibility of a layer by pressing the visibility icon.


## Deleting layers

The user can delete a layer by pressing the Delete button on that layer's controller. This will prompt the user before confirming the deletion of the layer. 