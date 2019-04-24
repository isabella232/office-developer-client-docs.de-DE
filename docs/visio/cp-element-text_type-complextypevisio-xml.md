---
title: CP-Element (text_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Markiert den Anfang einer Zeicheneigenschaften ausführen, die entsprechend dem entsprechenden Char-Element formatiert ist. Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282950"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a>CP-Element (text_Type complexType) (' Visio XML ')

Markiert den Anfang einer Zeicheneigenschaften ausführen, die entsprechend dem entsprechenden Char-Element formatiert ist. Die Ausführung wird am Ende des Texts oder bis zum nächsten Tag definiert.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Page #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Enthält den Text einer Form.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Der Char-Elementindex, der von dieser Eigenschaft ausgeführt wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

