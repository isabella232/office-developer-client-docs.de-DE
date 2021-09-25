---
title: PageContents-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Gibt die Informationen zu den Formen in einem Master- oder Zeichenblatt einer Zeichnung an.
ms.openlocfilehash: a87099a19480c90b18498009f5c0723de61a7427
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608172"
---
# <a name="pagecontents-element-visio-xml"></a>PageContents-Element (Visio XML)

Gibt die Informationen zu den Formen in einem Master- oder Zeichenblatt einer Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
|[Formen](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
   
### <a name="attributes"></a>Attribute

Keine.
  

