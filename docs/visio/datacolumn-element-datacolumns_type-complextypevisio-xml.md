---
title: DataColumn-Element (DataColumns_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Definiert, wie eine Datenspalte im Fenster Externe Daten auf der benutzeroberfläche Visio angezeigt wird, und qualifiziert die Daten in der Spalte, indem der Datentyp und die Formatierung definiert werden.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541225"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>DataColumn-Element (DataColumns_Type complexType) (Visio XML)

Definiert, wie eine Datenspalte im Fenster Externe Daten auf der benutzeroberfläche Visio angezeigt wird, und qualifiziert die Daten in der Spalte durch Definieren des Datentyps und der Formatierung.  
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Enthält alle **DataColumn-Elemente** in einem Daten recordset.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kalender  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Kalender-ID der Datenspalte.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |erforderlich  <br/> |Externer Name der Datenspalte. Wird in den Überschriften im Fenster **Externe Daten** und in Beschriftungen in Datengrafiken angezeigt.  <br/> |Werte des xsd:string-Typs.  <br/> |
|Währung  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Währungs-ID der Datenspalte.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> |Typ der Daten in der Datenspalte.  <br/> |Werte des Typs xsd:unsignedShort.  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den Grad (Leistung) der Einheiten an, z. B. quadratisch oder cubed. Der Standardwert (attribut absent) ist 1.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Definiert die Anzeigeposition der Datenspalte im Fenster Externe Daten von der linken Spalte (0) bis zur rechten Spalte (größter Wert).   <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Breite der Datenspalte im **Fenster Externe** Daten.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Datenspalte einen Hyperlink in einem Shape erstellt, wenn das Shape mit Daten verknüpft ist.  <br/> |Werte des typs xsd:boolean.  <br/> |
|Bezeichnung  <br/> |xsd:string  <br/> |erforderlich  <br/> |Bezeichnung der Datenspalte.  <br/> |Werte des xsd:string-Typs.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die Sprach-ID der Datenspalte.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Zugeordnet  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob die Spalte im Fenster Externe **Daten angezeigt** wird. True (1), damit die Spalte sichtbar ist; False (0), damit die Spalte nicht sichtbar ist. Der Standardwert (Attribut nicht vorhanden) ist, dass die Spalte sichtbar ist.  <br/> |Werte des typs xsd:boolean.  <br/> |
|Name  <br/> |xsd:string  <br/> |erforderlich  <br/> |Interner Name der Datenspalte. Wird als Zeilenname für das Shape-Data-Element (benutzerdefinierte Eigenschaft) verwendet, das einem Shape hinzugefügt wird, wenn das Shape mit einer Datenzeile verknüpft ist.  <br/> |Werte des xsd:string-Typs.  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |Optional  <br/> |Spaltenbeschriftung, die an Visio der zugrunde liegenden ADO-Schnittstelle zurückgegeben wird.  <br/> |Werte des xsd:string-Typs.  <br/> |
|UnitType  <br/> |xsd:string  <br/> |Optional  <br/> |Einheitentyp der Daten in der Datenspalte.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

