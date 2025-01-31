---
title: Section.PageNumberStart property (Publisher)
keywords: vbapb10.chm7405572
f1_keywords:
- vbapb10.chm7405572
ms.prod: publisher
api_name:
- Publisher.Section.PageNumberStart
ms.assetid: f4124b7d-4a90-2489-13da-947df0c34a3d
ms.date: 06/13/2019
ms.localizationpriority: medium
---


# Section.PageNumberStart property (Publisher)

Sets or returns the page number that the specified section starts with. Read/write **Long**.


## Syntax

_expression_.**PageNumberStart**

_expression_ A variable that represents a **[Section](Publisher.Section.md)** object.


## Return value

Long


## Example

The following example sets the starting page number for the first section of the active document to 45.

```vb
ActiveDocument.Sections(1).PageNumberStart = 45 

```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]