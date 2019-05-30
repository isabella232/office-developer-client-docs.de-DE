---
title: DataColumn-Element (DataColumns_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Definiert, wie eine Datenspalte im Fenster Externe Daten auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte, indem Sie den Datentyp und die Formatierung definiert.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541225"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn-Element (DataColumns_Type complexType) (Visio XML)

Definiert, wie eine Datenspalte im Fenster **externe Daten** auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte, indem Sie den Datentyp und die Formatierung definiert. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn** -Elemente in einem Datenrecordset.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kalender  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Kalender-ID der Datenspalte.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Spaltenname  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Externer Name der Datenspalte. Wird in den Überschriften im Fenster **externe Daten** und in Beschriftungen in Datengrafiken angezeigt.  <br/> |Werte des Typs XSD: String.  <br/> |
|Währung  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Währungs-ID der Datenspalte.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|DataType  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Typ der Daten in der Datenspalte.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Degree  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt den Grad (Leistung) der Einheiten an, beispielsweise Quadrat oder Würfel. Das Standardattribut (fehlend) ist 1.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Display Order  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Definiert die Anzeigeposition der Datenspalte im Fenster **externe Daten** von der linken Spalte (0) bis zur rechten Spalte (größter Wert).  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DisplayWidth  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Breite der Datenspalte im Fenster **externe Daten** .  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Hyperlink  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Datenspalte einen Hyperlink in einer Form erstellt, wenn das Shape mit Daten verknüpft ist.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Label  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Die Bezeichnung der Datenspalte.  <br/> |Werte des Typs XSD: String.  <br/> |
|LangID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die Sprachen-ID der Datenspalte.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Zugeordnet  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Spalte im Fenster **externe Daten** angezeigt wird. True (1), damit die Spalte sichtbar ist, andernfalls false. False (0), damit die Spalte nicht sichtbar ist. Das Standardattribut (fehlend) ist, dass die Spalte sichtbar ist.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Interner Name der Datenspalte. Wird als Zeilenname für das Shape-Datenelement (benutzerdefinierte Eigenschaft) verwendet, das einem Shape hinzugefügt wird, wenn das Shape mit einer Datenzeile verknüpft ist.  <br/> |Werte des Typs XSD: String.  <br/> |
|OrigLabel  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Spaltenbezeichnung zurückgegeben von der zugrunde liegenden ADO-Schnittstelle an Visio.  <br/> |Werte des Typs XSD: String.  <br/> |
|UnitType  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Einheit Typ der Daten in der Datenspalte.  <br/> |Werte des Typs XSD: String.  <br/> |
   

