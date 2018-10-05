---
title: Windows-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Enthält die Elemente des Fensters für ein Dokument an.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386803"
---
# <a name="windows-element-visio-xml"></a>Windows-Element ("Visio XML")

Enthält die Elemente des **Fensters** für ein Dokument an. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio.
  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|"ClientHeight"  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Stellt die Höhendimension einen Anzeigebereich  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|ClientWidth  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Stellt einen Anzeigebereich die Dimension Breite  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
   

