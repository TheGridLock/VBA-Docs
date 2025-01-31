---
title: Hyperlink.ScreenTip property (Access)
keywords: vbaac10.chm10119
f1_keywords:
- vbaac10.chm10119
ms.prod: access
api_name:
- Access.Hyperlink.ScreenTip
ms.assetid: b935ea5c-17d8-e3ad-fca2-ef0985daa709
ms.date: 03/20/2019
ms.localizationpriority: medium
---


# Hyperlink.ScreenTip property (Access)

Use the **ScreenTip** property to specify or determine the text that is displayed when you move the cursor over a hyperlink control. Read/write **String**.


## Syntax

_expression_.**ScreenTip**

_expression_ A variable that represents a **[Hyperlink](Access.Hyperlink.md)** object.


## Remarks

When you move the cursor over a hyperlink control whose **HyperlinkSubAddress** property is set, Microsoft Access changes the cursor to an upward-pointing hand and displays the text string defined by the **ScreenTip** property. Choosing the control displays the object or webpage specified by the link.

For more information about hyperlink addresses and their format, see the **[Hyperlink.Address](Access.Hyperlink.Address.md)** and **[Hyperlink.SubAddress](Access.Hyperlink.SubAddress.md)** property topics.


## Example

The following example displays the message "Go to Home page" when the cursor hovers over the hyperlink named "HomePage" on the **Order Entry** form.

```vb
Forms("Order Entry").Controls("HomePage").Hyperlink.ScreenTip = "Go to Home page"
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]