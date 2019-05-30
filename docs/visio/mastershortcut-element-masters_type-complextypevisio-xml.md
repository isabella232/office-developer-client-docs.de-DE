---
title: MasterShortcut-Element (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Gibt eine im Dokument definierte Master Verknüpfung an.
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538207"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>MasterShortcut-Element (Masters_Type complexType) (Visio XML)

Gibt eine im Dokument definierte Master Verknüpfung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Enthält die **Master** -Elemente für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt ein codiertes Binär Symbol (im ICO-Format) MIME (Multipurpose Internet Mail Extensions) für ein **Master** -oder **MasterShortcut** -Element in einem Dokument an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Gibt an, ob der Text des Elements im Schablonenfenster Links, rechts oder zentriert ausgerichtet ist.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|IconSize  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Die Größe des Elementsymbols.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der universelle Name des-Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|PatternFlags  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Bestimmt, ob sich ein Master-Shape wie ein benutzerdefiniertes Muster verhält.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Eingabeaufforderung  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Statusleiste und die QuickInfo-Eingabeaufforderung für das Element.  <br/> |Werte des Typs XSD: String.  <br/> |
|ShortcutHelp  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Eine Hilfezeichenfolge für das-Element.  <br/> |Werte des Typs XSD: String.  <br/> |
|ShortcutURL  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Eine URL zu einem **MasterShortcut** -Element.  <br/> |Werte des Typs XSD: String.  <br/> |
   

