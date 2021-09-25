---
title: DataConnection-Element (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrahiert die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer Nicht-XML-Datenquelle.
ms.openlocfilehash: c37c1076444febdc292fa91933b31f56413bc19e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563091"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a>DataConnection-Element (DataConnections_Type complexType) (Visio XML)

Abstrahiert die Kommunikation zwischen einem oder mehreren **DataRecordset-Elementen** und einer Nicht-XML-Datenquelle. 
  
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Dataconnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Enthält die **DataConnection-Elemente** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |Optional  <br/> |Der Standardwert ist false. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|Befehl  <br/> |xsd:string  <br/> |Optional  <br/> |Die Befehlszeichenfolge, die zum Abfragen der Datenquelle verwendet wird.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |Optional  <br/> |Die Verbindungszeichenfolge, die die Parameter definiert, die zum Herstellen einer Verbindung mit einer Datenquelle erforderlich sind.  <br/> |Werte des Typs "xsd:string".  <br/> |
|FileName  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Name der Verbindungsdatei. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des Typs "xsd:string".  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |Optional  <br/> |Ein vom Benutzer bereitgestellter Name für die Datenverbindung.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die id, die von Visio für eine bestimmte Verbindung zugewiesen wurde, eindeutig innerhalb des Dokuments.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die Wartezeit in Minuten beim Versuch, eine Verbindung herzustellen, bevor der Versuch beendet wird.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

