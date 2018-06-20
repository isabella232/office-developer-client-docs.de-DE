---
title: DataColumn-Element (DataColumns_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Definiert, wie eine Datenspalte im Fenster externe Daten in der Visio-Benutzeroberfläche angezeigt und berechtigt ist die Daten in der Spalte Datentyp zu definieren und die Formatierung.
ms.openlocfilehash: f74061b9f3b8f4b93d8aa0e97e4e7c1e45131cbd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796803"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn-Element (DataColumns_Type ComplexType) ("Visio XML")

Definiert, wie eine Datenspalte im Fenster **Externe Daten** in der Visio-Benutzeroberfläche angezeigt und berechtigt ist die Daten in der Spalte Datentyp zu definieren und die Formatierung. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn** -Elemente in einem Datenrecordset.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kalender  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Kalender-ID der Datenspalte.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |XSD: String  <br/> |erforderlich  <br/> |Externer Name der Datenspalte. Wird in der Überschriften in das Fenster **Externe Daten** und Beschriftungen in Datengrafiken angezeigt.  <br/> |Werte des Typs xsd: String.  <br/> |
|Währung  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Currency-ID der Datenspalte.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|DataType  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> |Typ der Daten in der Datenspalte.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|Grad  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt den Grad der Einheiten, beispielsweise im Quadrat oder hoch drei (Power). Der Standardwert (-Attribut nicht vorhanden) ist 1.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Definiert die Anzeigeposition der Datenspalte im Fenster **Externe Daten** aus der Spalte ganz links (0), um die Spalte ganz rechts (größten Wert).  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die Breite der Datenspalte im Fenster **Externe Daten** .  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Hyperlink  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Datenspalte einen Hyperlink in einem Shape erstellt, wenn das Shape mit Daten verknüpft ist.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Beschriftung  <br/> |XSD: String  <br/> |erforderlich  <br/> |Bezeichnung der Datenspalte.  <br/> |Werte des Typs xsd: String.  <br/> |
|LangID  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die Sprachen-ID der Datenspalte.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Zugeordnet sind  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Spalte im Fenster **Externe Daten** angezeigt wird. Legen Sie True (1) für die Spalte sichtbar sein; False (0) für die Spalte nicht sichtbar sein. Der Standardwert (-Attribut nicht vorhanden) ist für die Spalte sichtbar sein.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Name  <br/> |XSD: String  <br/> |erforderlich  <br/> |Interner Name der Datenspalte. Wird als Zeile mit dem Namen für die Shape-Datenelements (benutzerdefinierte Eigenschaft) mit einer Form hinzugefügt werden, wenn das Shape mit einer Datenzeile verknüpft ist.  <br/> |Werte des Typs xsd: String.  <br/> |
|OrigLabel  <br/> |XSD: String  <br/> |Optional  <br/> |Spalte Beschriftung durch die zugrunde liegende ADO-Schnittstelle an Visio zurückgegeben.  <br/> |Werte des Typs xsd: String.  <br/> |
|UnitType  <br/> |XSD: String  <br/> |Optional  <br/> |Unit-Typ der Daten in der Datenspalte.  <br/> |Werte des Typs xsd: String.  <br/> |
   

