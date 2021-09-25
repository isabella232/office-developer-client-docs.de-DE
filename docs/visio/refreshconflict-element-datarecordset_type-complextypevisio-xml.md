---
title: RefreshConflict-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Datenrecordsets in Konflikt steht.
ms.openlocfilehash: cc0bf49862465030fec0d0e1d1dfa7bff80a98b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573586"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a>RefreshConflict-Element (DataRecordSet_Type complexType) (Visio XML)

Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Datenrecordsets in Konflikt steht.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Seiten-ID des Shapes, das an dem Konflikt beteiligt ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Rowid  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die ursprüngliche Zeilen-ID der Zeile, die nach der Aktualisierung der Daten in Konflikt geraten ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Shape-ID des Shapes, das an dem Konflikt beteiligt ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

