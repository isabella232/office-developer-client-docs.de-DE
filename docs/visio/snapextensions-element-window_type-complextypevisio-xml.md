---
title: SnapExtensions-Element (Window_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Gibt an, ob eine bestimmte Ausrichtungs Erweiterungseinstellung für das aktive Fenster aktiviert oder deaktiviert ist. Der Wert kann eine Summe der Werte in der folgenden Tabelle sein.
ms.openlocfilehash: 57fde520d3dc8e0582c0062a599d5f38a73169b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334419"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>SnapExtensions-Element (Window_Type complexType) (' Visio XML ')

Gibt an, ob eine bestimmte Ausrichtungs Erweiterungseinstellung für das aktive Fenster aktiviert oder deaktiviert ist. Der Wert kann eine Summe der Werte in der folgenden Tabelle sein.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Windows. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  
## <a name="remarks"></a>Bemerkungen

Der Wert des **SnapExtensions** -Elements kann eine Summe der Werte in der folgenden Tabelle sein. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Nicht ausrichten.  <br/> |
|1  <br/> |Ausrichtungsfeld Erweiterung.  <br/> |
|2  <br/> |An der Mittelachse anDocken.  <br/> |
|4  <br/> |An Kurventangenten Erweiterung ausrichten.  <br/> |
|8  <br/> |An Endpunkt Erweiterung ausrichten.  <br/> |
|16  <br/> |AnDocken an Mittelpunkt.  <br/> |
|32  <br/> |An lineare Erweiterung ausrichten.  <br/> |
|64  <br/> |An Kurven Erweiterung ausrichten.  <br/> |
|128  <br/> |An Endpunkt senkrecht anDocken.  <br/> |
|256  <br/> |An Mittelpunkt senkrecht anDocken.  <br/> |
|512  <br/> |An Endpunkt horizontaler Durchwahl ausrichten.  <br/> |
|1024  <br/> |Ausrichtung an Endpunkt vertikaler Durchwahl.  <br/> |
|2048  <br/> |An Ellipse Center-Erweiterung ausrichten.  <br/> |
|4096  <br/> |An isometrische Winkel Erweiterung ausrichten.  <br/> |
   

