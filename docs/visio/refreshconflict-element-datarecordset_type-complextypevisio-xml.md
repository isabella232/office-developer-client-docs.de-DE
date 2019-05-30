---
title: RefreshConflict-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Daten-Recordsets in Konflikt steht.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542835"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>RefreshConflict-Element (DataRecordSet_Type complexType) (Visio XML)

Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Daten-Recordsets in Konflikt steht.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Seiten-ID der Form, die an dem Konflikt beteiligt ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ROWID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ursprüngliche Zeilen-ID der Zeile, die nach dem Aktualisieren der Daten jetzt in Konflikt steht.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ShapeID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Shape-ID der Form, die an dem Konflikt beteiligt ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

