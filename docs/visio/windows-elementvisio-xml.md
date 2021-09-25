---
title: Windows-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Enthält die Window-Elemente für ein Dokument.
ms.openlocfilehash: ac007299f7f73c5839d2ea735f2dcd7a186cf178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553627"
---
# <a name="windows-element-visio-xml"></a>Windows-Element (Visio XML)

Enthält die **Window-Elemente** für ein Dokument. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Stellt die Höhe eines Anzeigebereichs dar.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|ClientWidth  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Stellt die Breite eines Anzeigebereichs dar.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
   

