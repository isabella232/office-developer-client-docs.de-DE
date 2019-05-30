---
title: SnapExtensions-Element (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Gibt an, ob eine bestimmte Einstellung für die Ausrichtungs Erweiterung für das aktive Fenster aktiviert oder deaktiviert ist.
ms.openlocfilehash: 86ff7f32d6e12b2f0d7a8387d8e5b7ae9870b5fa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540378"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>SnapExtensions-Element (DocumentSettings_Type complexType) (Visio XML)

Gibt an, ob eine bestimmte Einstellung für die Ausrichtungs Erweiterung für das aktive Fenster aktiviert oder deaktiviert ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die Dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>Hinweise

Der Wert des **SnapExtensions** -Elements kann eine Summe der Werte in der folgenden Tabelle sein. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |Erweiterung für Ausrichtungsfeld ausrichten.  <br/> |
|2  <br/> |Ausrichten an der Mittelachse-Erweiterung.  <br/> |
|4  <br/> |An Kurve tangentiale Erweiterung ausrichten.  <br/> |
|8  <br/> |An Endpunkt Erweiterung ausrichten.  <br/> |
|16  <br/> |An Mittelpunkt Erweiterung ausrichten.  <br/> |
|32  <br/> |An lineare Erweiterung ausrichten.  <br/> |
|64  <br/> |An Kurven Erweiterung ausrichten.  <br/> |
|128  <br/> |Lotrechte Erweiterung an Endpunkt ausrichten.  <br/> |
|256  <br/> |Senkrecht zur Mitte ausrichten.  <br/> |
|512  <br/> |Horizontale Erweiterung an Endpunkt ausrichten.  <br/> |
|1024  <br/> |Vertikale Erweiterung an Endpunkt ausrichten.  <br/> |
|2048  <br/> |An Ellipse Center-Erweiterung ausrichten.  <br/> |
|4096  <br/> |Andocken an isometrischer Winkel Erweiterung.  <br/> |
   

