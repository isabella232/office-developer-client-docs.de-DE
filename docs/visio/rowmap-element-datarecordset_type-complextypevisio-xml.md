---
title: RowMap-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Karten einer Datensatzzeile zu einem Shape.
ms.openlocfilehash: 250829c1199e4936bbdef91fdf3ba61873ff54fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607780"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a>RowMap-Element (DataRecordSet_Type complexType) (Visio XML)

Karten einer Datensatzzeile zu einem Shape.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

****

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Seiten-ID des Shapes, das mit Daten in der Datenrecordsetzeile verknüpft ist, die durch **RowID** identifiziert wird.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Rowid  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Zeilen-ID der Zeile, eindeutig innerhalb des Datenrecordsets.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Shape-ID des Shapes, das mit Daten in der Datenrecordsetzeile verknüpft ist, die durch **RowID** identifiziert wird.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

