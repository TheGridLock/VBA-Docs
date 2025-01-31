---
title: ConnectorFormat object (Publisher)
keywords: vbapb10.chm3276799
f1_keywords:
- vbapb10.chm3276799
ms.prod: publisher
api_name:
- Publisher.ConnectorFormat
ms.assetid: 9b541d54-b1b9-c023-c9c4-08ff6b811eb9
ms.date: 05/31/2019
ms.localizationpriority: medium
---


# ConnectorFormat object (Publisher)

Contains properties and methods that apply to connectors. A connector is a line that attaches two other shapes at points called connection sites. If you rearrange shapes that are connected, the geometry of the connector will be automatically adjusted so that the shapes remain connected.
 
## Remarks

Use the **ConnectorFormat** property of the **[Shape](Publisher.Shape.md)** object or the **[ShapeRange](Publisher.ShapeRange.md)** collection to return a **ConnectorFormat** object. 

Use the **BeginConnect** and **EndConnect** methods of the **ConnectorFormat** object to attach the ends of the connector to other shapes in the publication. 

Use the **[RerouteConnections](Publisher.Shape.RerouteConnections.md)** method of the **Shape** object and **ShapeRange** collection to automatically find the shortest path between the two shapes connected by the connector. 

Use the **[Connector](Publisher.Shape.Connector.md)** property to determine whether a shape is a connector.

> [!NOTE] 
> You assign a size and a position when you add a connector to the **Shapes** collection, but the size and position are automatically adjusted when you attach the beginning and end of the connector to other shapes in the collection. Therefore, if you intend to attach a connector to other shapes, the initial size and position that you specify are irrelevant. Likewise, you specify which connection sites on a shape to attach the connector to when you attach the connector, but using the **RerouteConnections** method after the connector is attached may change which connection sites the connector attaches to, making your original choice of connection sites irrelevant.

## Example

The following example adds two rectangles to the active publication and then connects them with a curved connector.
 
```vb
Dim shpAll As Shapes 
Dim firstRect As Shape 
Dim secondRect As Shape 
 
Set shpAll = ActiveDocument.Pages(1).Shapes 
Set firstRect = shpAll.AddShape(Type:=msoShapeRectangle, _ 
 Left:=100, Top:=50, Width:=200, Height:=100) 
Set secondRect = shpAll.AddShape(Type:=msoShapeRectangle, _ 
 Left:=300, Top:=300, Width:=200, Height:=100) 

```


```vb
With shpAll.AddConnector(Type:=msoConnectorCurve, BeginX:=0, _ 
 BeginY:=0, EndX:=0, EndY:=0).ConnectorFormat 
 .BeginConnect ConnectedShape:=firstRect, ConnectionSite:=1 
 .EndConnect ConnectedShape:=secondRect, ConnectionSite:=1 
 .Parent.RerouteConnections 
End With
```


## Methods

- [BeginConnect](Publisher.ConnectorFormat.BeginConnect.md)
- [BeginDisconnect](Publisher.ConnectorFormat.BeginDisconnect.md)
- [EndConnect](Publisher.ConnectorFormat.EndConnect.md)
- [EndDisconnect](Publisher.ConnectorFormat.EndDisconnect.md)

## Properties

- [Application](Publisher.ConnectorFormat.Application.md)
- [BeginConnected](Publisher.ConnectorFormat.BeginConnected.md)
- [BeginConnectedShape](Publisher.ConnectorFormat.BeginConnectedShape.md)
- [BeginConnectionSite](Publisher.ConnectorFormat.BeginConnectionSite.md)
- [EndConnected](Publisher.ConnectorFormat.EndConnected.md)
- [EndConnectedShape](Publisher.ConnectorFormat.EndConnectedShape.md)
- [EndConnectionSite](Publisher.ConnectorFormat.EndConnectionSite.md)
- [Parent](Publisher.ConnectorFormat.Parent.md)
- [Type](Publisher.ConnectorFormat.Type.md)

## See also

- [Publisher Object Model Reference](overview/publisher/object-model.md)



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]