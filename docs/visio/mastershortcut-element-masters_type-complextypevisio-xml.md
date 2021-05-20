---
title: MasterShortcut-Element (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Gibt eine im Dokument definierte Masterverknüpfung an.
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538207"
---
# <a name="mastershortcut-element-masters_type-complextype-visio-xml"></a>MasterShortcut-Element (Masters_Type complexType) (Visio XML)

Gibt eine im Dokument definierte Masterverknüpfung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Enthält die **Master-Elemente** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt ein MIME(Multipurpose Internet Mail Extensions) codiertes binäres Symbol (im ICO-Format) für ein **Master-** oder **MasterShortcut-Element** in einem Dokument an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Gibt an, ob der Text des Elements im Schablonenfenster links, rechts oder zentriert ausgerichtet ist.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Die Größe des Symbols des Elements.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Bestimmt, ob sich ein Master-Shape wie ein benutzerdefiniertes Muster verhält.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|Eingabeaufforderung  <br/> |xsd:string  <br/> |Optional  <br/> |Die Statusleiste und die QuickInfo-Eingabeaufforderung für das Element.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ShortcutHelp  <br/> |xsd:string  <br/> |Optional  <br/> |Eine Hilfszeichenfolge für das Element.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ShortcutURL  <br/> |xsd:string  <br/> |Optional  <br/> |Eine URL zu einem **MasterShortcut-Element.**  <br/> |Werte des xsd:string-Typs.  <br/> |
   

