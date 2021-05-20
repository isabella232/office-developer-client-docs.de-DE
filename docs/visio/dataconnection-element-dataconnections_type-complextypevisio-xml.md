---
title: DataConnection-Element (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrahiert die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer Nicht-XML-Datenquelle.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538403"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>DataConnection-Element (DataConnections_Type complexType) (Visio XML)

Abstrahiert die Kommunikation zwischen einem oder **mehreren DataRecordset-Elementen** und einer Nicht-XML-Datenquelle. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |connections.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Enthält die **DataConnection-Elemente** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |Optional  <br/> |Der Standardwert ist false. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des typs xsd:boolean.  <br/> |
|Get-Help  <br/> |xsd:string  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen der Datenquelle verwendet wird.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |Optional  <br/> |Die Verbindungszeichenfolge, die die parameter definiert, die zum Herstellen einer Verbindung mit einer Datenquelle erforderlich sind.  <br/> |Werte des xsd:string-Typs.  <br/> |
|FileName  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Name der Verbindungsdatei. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des xsd:string-Typs.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |Optional  <br/> |Ein Benutzer hat den Namen für die Datenverbindung angegeben.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die id, die Visio für eine bestimmte Verbindung zugewiesen wird, die innerhalb des Dokuments eindeutig ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die Wartezeit in Minuten beim Versuch, eine Verbindung herzustellen, bevor der Versuch beendet wird.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
   

