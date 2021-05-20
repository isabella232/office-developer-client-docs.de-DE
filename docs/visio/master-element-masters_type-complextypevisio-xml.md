---
title: Master-Element (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Enthält Elemente, die einen Master für das Dokument definieren.
ms.openlocfilehash: 83727b89eaf44aae5dddecacff1f05f369ee0bf0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538046"
---
# <a name="master-element-masters_type-complextype-visio-xml"></a>Master-Element (Masters_Type complexType) (Visio XML)

Enthält Elemente, die einen Master für das Dokument definieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt ein MIME(Multipurpose Internet Mail Extensions) codiertes binäres Symbol (im ICO-Format) für ein **Master-** oder **MasterShortcut-Element** in einem Dokument an.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die das Seitenblatt für ein Page- oder **Master-Element** definieren.   <br/> |
|Formen  <br/> |Shapes_Type  <br/> |Enthält eine Auflistung von **Shape-Elementen.**  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Gibt an, ob der Mastertext im Schablonenfenster links, rechts oder zentriert ausgerichtet ist.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd:string  <br/> |Optional  <br/> |Eine GUID (global eindeutiger Bezeichner), die den Master in allen Dokumenten identifiziert.  <br/> |Werte des xsd:string-Typs.  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der Master auf der Benutzeroberfläche ausgeblendet ist.  <br/> |Werte des typs xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Die Größe des Symbols des Elements.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob das Symbol automatisch vom Master selbst generiert wird.  <br/> |Werte des typs xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Bestimmt, wie Microsoft Visio entscheidet, ob bereits ein Dokumentmaster vorhanden ist, wenn eine Instanz eines Masters auf dem Zeichenblatt abgelegt wird.  <br/> |Werte des typs xsd:boolean.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Bestimmt, ob sich ein Master-Shape wie ein benutzerdefiniertes Muster verhält.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|Eingabeaufforderung  <br/> |xsd:string  <br/> |Optional  <br/> |Die Statusleiste und die QuickInfo-Eingabeaufforderung für das Element.  <br/> |Werte des xsd:string-Typs.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Eine GUID, die den Master innerhalb des Dokuments identifiziert.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

