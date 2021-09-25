---
title: DataRecordSets-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Enthält alle DataRecordset-Elemente im Dokument.
ms.openlocfilehash: 2465739067d0103e6e90cbb18c1cef6fc251732e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608263"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Enthält alle **DataRecordset-Elemente** im Dokument.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des aktiven Datenrecordsets im Fenster **"Externe Daten",** wenn das Fenster geschlossen wird, sodass es beim nächsten Öffnen des Fensters wiederhergestellt werden kann.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|DataWindowOrder  <br/> |xsd:string  <br/> |Optional  <br/> |Die Reihenfolge der Datenrecordsets, die auf den Registerkarten des Fensters **"Externe Daten"** angezeigt werden. Eine sortierte Liste von Datenrecordset-IDs, getrennt durch Semikolons.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NextID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Die nächste verfügbare ID für ein neues Datenrecordset.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

