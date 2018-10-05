---
title: DataRecordSets-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c75b3233-9ac5-d29c-a658-d554e86e6be4
description: Enthält alle DataRecordset-Elemente im Dokument.
ms.openlocfilehash: 7730e55f0025181db193a1e64226e879f9072e90
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401489"
---
# <a name="datarecordsets-element-visio-xml"></a>DataRecordSets-Element ("Visio XML")

Enthält alle **DataRecordset** -Elemente im Dokument. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Recordsets.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataRecordSets" type="DataRecordSets_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Enthält alle **DataRecordset** -Elemente im Dokument.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ActiveRecordsetID  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des aktiven Datenrecordsets im Fenster **Externe Daten** , wenn die Fenster wird geschlossen, damit das alles sein kann das nächste Mal das Fenster wiederhergestellt wird geöffnet.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|DataWindowOrder  <br/> |XSD: String  <br/> |Optional  <br/> |Die Reihenfolge der Datenrecordsets auf den Registerkarten des Fensters für **Externe Daten** angezeigt. Eine sortierte Liste der IDs von Datenrecordset, getrennt durch Semikolons ein.  <br/> |Werte des Typs xsd: String.  <br/> |
|NextID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die nächste verfügbare ID für einen neuen Datenrecordset.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

