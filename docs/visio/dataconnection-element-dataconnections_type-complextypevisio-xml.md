---
title: DataConnection-Element (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrahiert die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer nicht-XML-Datenquelle.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538403"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>DataConnection-Element (DataConnections_Type complexType) (Visio XML)

Abstrahiert die Kommunikation zwischen einem oder mehreren **** DataRecordset-Elementen und einer nicht-XML-Datenquelle. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Connections. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Enthält die **** DataConnection-Elemente für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Der Standardwert ist false. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Befehl  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen der Datenquelle verwendet wird.  <br/> |Werte des Typs XSD: String.  <br/> |
|ConnectionString  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Verbindungszeichenfolge, die die Parameter definiert, die zum Herstellen einer Verbindung mit einer Datenquelle erforderlich sind.  <br/> |Werte des Typs XSD: String.  <br/> |
|FileName  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Der Name der Verbindungsdatei. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des Typs XSD: String.  <br/> |
|FriendlyName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Ein vom Benutzer bereitgestellter Name für die Datenverbindung.  <br/> |Werte des Typs XSD: String.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die von Visio für eine bestimmte Verbindung zugewiesene ID, die innerhalb des Dokuments eindeutig ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Timeout  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die Wartezeit in Minuten beim Versuch, eine Verbindung herzustellen, bevor Sie den Versuch beenden.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

