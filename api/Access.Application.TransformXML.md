---
title: Application.TransformXML method (Access)
keywords: vbaac10.chm12606
f1_keywords:
- vbaac10.chm12606
ms.prod: access
api_name:
- Access.Application.TransformXML
ms.assetid: 03b483ad-9785-be26-4632-411d8fc8a19d
ms.date: 02/05/2019
ms.localizationpriority: medium
---


# Application.TransformXML method (Access)

Applies an Extensible Stylesheet Language (XSL) stylesheet to an XML data file and writes the resulting XML to an XML data file.


## Syntax

_expression_.**TransformXML** (_DataSource_, _TransformSource_, _OutputTarget_, _WellFormedXMLOutput_, _ScriptOption_)

_expression_ A variable that represents an **[Application](Access.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _DataSource_|Required|**String**|The name and path of the XML file to import.|
| _TransformSource_|Required|**String**|The name and path to the XSL file to apply to the XML data file.|
| _OutputTarget_|Required|**String**|The file name and path for the resulting XML data file after applying the XSL file.|
| _WellFormedXMLOutput_|Optional|**Boolean**|Setting this argument to **True** will create a well-formed XML file. Setting this argument to **False** will encode the resulting XML file in UTF-16 format. The default value is **False**.|
| _ScriptOption_|Optional|**[AcTransformXMLScriptOption](Access.AcTransformXMLScriptOption.md)**|An **AcTransformXMLScriptOption** constant that specifies the action taken if the XSL file contains scripting code. The default value is **acPromptScript**.|

## Return value

Nothing


## Remarks

Setting the _WellFormedXMLOutput_ argument to **True** will result in a run-time error if the XSL file that you apply does not result in well-formed XML.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]