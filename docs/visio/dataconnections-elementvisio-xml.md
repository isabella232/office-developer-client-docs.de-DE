---
title: DataConnections-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Enthält die DataConnection-Elemente für das Dokument.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344492"
---
# <a name="dataconnections-element-visio-xml"></a>DataConnections-Element (' Visio XML ')

Enthält die **DataConnection** -Elemente für das Dokument. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Connections. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataConnection](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |Abstrahiert die Kommunikation zwischen einem oder mehreren **** DataRecordset-Elementen und einer nicht-XML-Datenquelle.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|NextID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die nächste verfügbare ID für neue Verbindungen.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

