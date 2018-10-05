---
title: MasterShortcut-Element (Masters_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Gibt ein master-Verknüpfung im Dokument definierten an.
ms.openlocfilehash: 03196c6fc1f3424c61bcce406dc050f2d5a73365
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392956"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>MasterShortcut-Element (Masters_Type ComplexType) ("Visio XML")

Gibt ein master-Verknüpfung im Dokument definierten an.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Master-Shape # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Enthält die **Master** -Elemente für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt an, dass ein MIME (Multipurpose Internet Mail Extensions) binary-Symbol (ICO-Format) für ein **Master-Shape** oder **MasterShortcut** -Element in einem Dokument codiert.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Gibt an, ob der Text des Elements im Schablonenfenster links, rechts ausgerichtet oder zentriert.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Die Größe des Symbols für das Element.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Bestimmt, ob ein Master-Shape als benutzerdefiniertes Muster verhält.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|Eingabeaufforderung  <br/> |XSD: String  <br/> |Optional  <br/> |Das Tool und die Statusleiste Tipp Aufforderung für das Element.  <br/> |Werte des Typs xsd: String.  <br/> |
|ShortcutHelp  <br/> |XSD: String  <br/> |Optional  <br/> |Ein Hilfetext für das Element.  <br/> |Werte des Typs xsd: String.  <br/> |
|ShortcutURL  <br/> |XSD: String  <br/> |Optional  <br/> |Eine URL zu einem **MasterShortcut** -Element.  <br/> |Werte des Typs xsd: String.  <br/> |
   

