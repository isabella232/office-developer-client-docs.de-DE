---
title: SnapExtensions-Element (DocumentSettings_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Gibt an, ob eine Einstellung für bestimmte Snap-In-Erweiterung aktiviert oder für das aktive Fenster deaktiviert ist.
ms.openlocfilehash: 4c00d8d45c1eb33f57f727779db91e358a83a969
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798139"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>SnapExtensions-Element (DocumentSettings_Type ComplexType) ("Visio XML")

Gibt an, ob eine Einstellung für bestimmte Snap-In-Erweiterung aktiviert oder für das aktive Fenster deaktiviert ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>Bemerkungen

Der Wert des **SnapExtensions** -Elements kann die Summe der Werte in der folgenden Tabelle werden. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |An Ausrichtungsfeld-Erweiterung ausrichten.  <br/> |
|2  <br/> |Center Achse Erweiterung ausrichten.  <br/> |
|4  <br/> |Kurve Tangenten Erweiterung ausrichten.  <br/> |
|8  <br/> |Endpunkt-Erweiterung ausrichten.  <br/> |
|16  <br/> |Mittelpunkt Erweiterung ausrichten.  <br/> |
|32  <br/> |Lineare Erweiterung ausrichten.  <br/> |
|64  <br/> |Erweiterung der Kurve ausrichten.  <br/> |
|128  <br/> |Endpunkt senkrecht Erweiterung ausrichten.  <br/> |
|256  <br/> |Mittelpunkt perpendicular Erweiterung ausrichten.  <br/> |
|512  <br/> |Horizontale Erweiterung Endpunkt ausrichten.  <br/> |
|1024  <br/> |Vertikale Erweiterung Endpunkt ausrichten.  <br/> |
|2048  <br/> |Ellipse Center Erweiterung ausrichten.  <br/> |
|4096  <br/> |Isometrische Winkel Erweiterung ausrichten.  <br/> |
   

