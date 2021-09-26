---
title: Master-Element (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Enthält Elemente, die ein Master-Shape für das Dokument definieren.
ms.openlocfilehash: 9bed3001bdf40fe54a32e6680c5de92a3035442f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603529"
---
# <a name="master-element-masters_type-complextype-visio-xml"></a>Master-Element (Masters_Type complexType) (Visio XML)

Enthält Elemente, die ein Master-Shape für das Dokument definieren.
  
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Enthält die **Masterelemente** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Gibt ein MIME(Multipurpose Internet Mail Extensions) codiertes Binärsymbol (im ICO-Format) für ein **Master-** oder **MasterShortcut-Element** in einem Dokument an.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die das Seitenblatt für ein **Page-** oder **Master-Element** definieren.  <br/> |
|Formen  <br/> |Shapes_Type  <br/> |Enthält eine Auflistung von **Shape-Elementen.**  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Gibt an, ob der Text des Master-Shapes im Schablonenfenster links, rechts oder zentriert ausgerichtet wird.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|BaseID  <br/> |xsd:string  <br/> |Optional  <br/> |Eine GUID (global eindeutiger Bezeichner), die das Master-Shape dokumentübergreifend identifiziert.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob das Master-Shape auf der Benutzeroberfläche ausgeblendet ist.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Die Größe des Symbols des Elements.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob das Symbol automatisch vom Master selbst generiert wird.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Bestimmt, wie Microsoft Visio entscheidet, ob ein Dokumentmaster bereits vorhanden ist, wenn eine Instanz eines Master-Shapes auf dem Zeichenblatt abgelegt wird.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Bestimmt, ob sich ein Master-Shape wie ein benutzerdefiniertes Muster verhält.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|Eingabeaufforderung  <br/> |xsd:string  <br/> |Optional  <br/> |Die Eingabeaufforderung der Statusleiste und der QuickInfo für das Element.  <br/> |Werte des Typs "xsd:string".  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Eine GUID, die das Master-Shape im Dokument identifiziert.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

