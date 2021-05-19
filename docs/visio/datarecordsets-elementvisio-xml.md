---
title: DataRecordSets-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Enthält alle DataRecordset-Elemente im Dokument.
ms.openlocfilehash: efa7d58eabc1b1192862dbbe090ddd5008947c1d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542443"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets-Element (Visio XML)

Enthält alle **DataRecordset-Elemente** im Dokument. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Enthält alle **DataRecordset-Elemente** im Dokument.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des aktiven Datendatensatz im Fenster Externe Daten, wenn das Fenster geschlossen wird, sodass es beim nächsten Öffnen des Fensters wiederhergestellt werden kann.   <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |Optional  <br/> |Die Reihenfolge der Datendatensätze, die auf den Registerkarten des Fensters Externe **Daten angezeigt** werden. Eine geordnete Liste von Daten-Recordset-IDs, getrennt durch Semikolonen.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die nächste verfügbare ID für ein neues Daten recordset.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
   

