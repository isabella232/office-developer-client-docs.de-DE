---
title: DataRecordSets-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Enthält alle dataRecordset-Elemente im Dokument.
ms.openlocfilehash: 7730e55f0025181db193a1e64226e879f9072e90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360326"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets-Element (' Visio XML ')

Enthält alle dataRecordset-Elemente im Dokument. **** 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Recordsets. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Enthält alle dataRecordset-Elemente im Dokument. ****  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID des aktiven Datenrecordset im Fenster **externe Daten** , wenn das Fenster geschlossen wird, sodass es beim nächsten Öffnen des Fensters wiederhergestellt werden kann.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DataWindowOrder  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Reihenfolge der Datenrecordset, die auf den Registerkarten des Fensters **externe Daten** angezeigt werden. Eine sortierte Liste von Datensatzgruppen-IDs, getrennt durch Semikolons.  <br/> |Werte des XSD: String-Typs.  <br/> |
|NextID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die nächste verfügbare ID für ein neues Datenrecordset.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

