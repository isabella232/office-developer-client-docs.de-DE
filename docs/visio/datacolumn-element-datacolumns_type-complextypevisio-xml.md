---
title: DataColumn-Element (DataColumns_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Definiert, wie eine Datenspalte im Fenster Externe Daten auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.
ms.openlocfilehash: 453ff44131575bd3d6927fdddb81db5f3f431a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344821"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn-Element (DataColumns_Type complexType) (' Visio XML ')

Definiert, wie eine Datenspalte im Fenster **externe Daten** auf der Visio-Benutzeroberfläche angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|Kalender  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Die Kalender-ID der Datenspalte.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|ColumnName-Nr.  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Externer Name der Datenspalte. Wird in den Überschriften im Fenster **externe Daten** und in Beschriftungen in Datengrafiken angezeigt.  <br/> |Werte des XSD: String-Typs.  <br/> |
|Währung  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Währungs-ID der Datenspalte.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|DataType  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> |Der Typ der Daten in der Datenspalte.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Degree  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt den Grad (Potenz) der Einheiten an, beispielsweise quadriert oder gewürfelt. Der Standardwert (das Attribut fehlt) ist 1.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Display Order  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Definiert die Anzeigeposition der Datenspalte im Fenster **externe Daten** , von der linken Spalte (0) bis zur rechten Spalte (größter Wert).  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DisplayWidth  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Breite der Datenspalte im Fenster **externe Daten** .  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Hyperlink  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Datenspalte in einem Shape einen Hyperlink erstellt, wenn die Form mit Daten verknüpft ist.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Label  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Bezeichnung der Datenspalte.  <br/> |Werte des XSD: String-Typs.  <br/> |
|LangID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die Sprach-ID der Datenspalte.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Zugeordnet  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob die Spalte im Fenster **externe Daten** angezeigt wird. True (1), damit die Spalte sichtbar ist; False (0), damit die Spalte nicht sichtbar ist. Der Standardwert (fehlendes Attribut) ist, dass die Spalte sichtbar ist.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Interner Name der Datenspalte. Wird als Zeilenname für das Shape-Datenelement (benutzerdefinierte Eigenschaft) verwendet, das einem Shape hinzugefügt wird, wenn das Shape mit einer Datenzeile verknüpft ist.  <br/> |Werte des XSD: String-Typs.  <br/> |
|OrigLabel  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Spaltenbeschriftung wird von der zugrunde liegenden ADO-Schnittstelle an Visio zurückgegeben.  <br/> |Werte des XSD: String-Typs.  <br/> |
|UnitType  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Einheitentyp der Daten in der Datenspalte.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

