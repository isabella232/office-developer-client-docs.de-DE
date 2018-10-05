---
title: Master-Element (Masters_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Enthält Elemente, die ein Master-Shape für das Dokument zu definieren.
ms.openlocfilehash: f6effa521b7c5ea69d41b6770ee2dbef61af097c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400488"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Master-Element (Masters_Type ComplexType) ("Visio XML")

Enthält Elemente, die ein Master-Shape für das Dokument zu definieren.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt an, dass ein MIME (Multipurpose Internet Mail Extensions) binary-Symbol (ICO-Format) für ein **Master-Shape** oder **MasterShortcut** -Element in einem Dokument codiert.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, mit die das Seitenblatt eines **Zeichenblatts** oder des **Masters** -Elements definiert.  <br/> |
|Shapes  <br/> |Shapes_Type  <br/> |Enthält eine Auflistung von **Shape** -Elementen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Gibt an, ob das Master-Shape-Text im Schablonenfenster links, rechts ausgerichtet oder zentriert.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|BaseID  <br/> |XSD: String  <br/> |Optional  <br/> |Eine GUID (globally unique Identifier), das Master-Shape in Dokumenten identifiziert.  <br/> |Werte des Typs xsd: String.  <br/> |
|Ausgeblendet  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob das Master-Shape auf der Benutzeroberfläche ausgeblendet ist.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Die Größe des Symbols für das Element.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob das Symbol des Master-Objekts automatisch generiert wird.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Bestimmt, wie Microsoft Visio entscheidet, wenn ein Dokumentmaster bereits vorhanden, wenn eine Instanz der ist ein Master-Shape auf dem Zeichenblatt abgelegt wird.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Bestimmt, ob ein Master-Shape als benutzerdefiniertes Muster verhält.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|Eingabeaufforderung  <br/> |XSD: String  <br/> |Optional  <br/> |Das Tool und die Statusleiste Tipp Aufforderung für das Element.  <br/> |Werte des Typs xsd: String.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |Optional  <br/> |Eine GUID, die das Master-Shape innerhalb des Dokuments identifiziert.  <br/> |Werte des Typs xsd: String.  <br/> |
   

