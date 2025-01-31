---
title: ListBox.AfterUpdate property (Access)
keywords: vbaac10.chm11279
f1_keywords:
- vbaac10.chm11279
ms.prod: access
api_name:
- Access.ListBox.AfterUpdate
ms.assetid: b71e1b7a-6893-505b-6de8-b877190c76d6
ms.date: 02/12/2019
ms.localizationpriority: medium
---


# ListBox.AfterUpdate property (Access)

Returns or sets which macro, event procedure, or user-defined function runs when the **[AfterUpdate](access.listbox.afterupdate-event.md)** event occurs. Read/write **String**.


## Syntax

_expression_.**AfterUpdate**

_expression_ A variable that represents a **[ListBox](Access.ListBox.md)** object.


## Remarks

Valid values for this property are:

- _macroname_, where _macroname_ is the name of a macro.

- [Event Procedure], which indicates the event procedure associated with the **AfterUpdate** event for the specified object.

- _=functionname()_, where _functionname_ is the name of a user-defined function.


## Example

The following example specifies that when the **AfterUpdate** event occurs on the first form of the current project, the associated event procedure should run.


```vb
Forms(0).AfterUpdate = "[Event Procedure]" 

```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]