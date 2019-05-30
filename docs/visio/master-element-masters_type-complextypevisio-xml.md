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
# <a name="master-element-masterstype-complextype-visio-xml"></a>Master-Element (Masters_Type complexType) (Visio XML)

Enthält Elemente, die einen Master für das Dokument definieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Masters. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt ein codiertes Binär Symbol (im ICO-Format) MIME (Multipurpose Internet Mail Extensions) für ein **Master** -oder **MasterShortcut** -Element in einem Dokument an.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die das Seitenblatt für ein **Page** -oder **Master** -Element definieren.  <br/> |
|Formen  <br/> |Shapes_Type  <br/> |Enthält eine Auflistung von **Shape** -Elementen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Gibt an, ob der Text des Masters im Schablonenfenster Links, rechts oder zentriert ausgerichtet ist.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|BaseID  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Eine GUID (Globally Unique Identifier), die den Master Across Documents identifiziert.  <br/> |Werte des Typs XSD: String.  <br/> |
|Hidden  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Master in der Benutzeroberfläche ausgeblendet ist.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IconSize  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Die Größe des Elementsymbols.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|IconUpdate  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob das Symbol automatisch aus dem Master selbst generiert wird.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|MatchByName  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Legt fest, wie Microsoft Visio entscheidet, ob ein Dokumentmaster bereits vorhanden ist, wenn eine Instanz eines Masters auf dem Zeichenblatt abgelegt wird.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der universelle Name des-Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|PatternFlags  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Bestimmt, ob sich ein Master-Shape wie ein benutzerdefiniertes Muster verhält.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Eingabeaufforderung  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Statusleiste und die QuickInfo-Eingabeaufforderung für das Element.  <br/> |Werte des Typs XSD: String.  <br/> |
|UniqueID  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Eine GUID, mit der der Master im Dokument identifiziert wird.  <br/> |Werte des Typs XSD: String.  <br/> |
   

