---
title: DataConnection-Element (DataConnections_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Fasst die Kommunikation zwischen einem oder mehreren DataRecordset-Elementen und einer nicht auf XML basierenden Datenquelle zusammen.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399424"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a>DataConnection-Element (DataConnections_Type ComplexType) ("Visio XML")

Fasst die Kommunikation zwischen einem oder mehreren **DataRecordset** -Elementen und einer nicht auf XML basierenden Datenquelle zusammen. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DataConnection_Type](dataconnection_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Connections.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DataConnections](dataconnections-elementvisio-xml.md) <br/> |[DataConnections_Type](dataconnections_type-complextypevisio-xml.md) <br/> |Enthält die **DataConnection** -Elemente für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Der Standardwert ist false. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Command  <br/> |XSD: String  <br/> |Optional  <br/> |Die Befehlszeichenfolge wird zum Abfragen der Datenquelle verwendet.  <br/> |Werte des Typs xsd: String.  <br/> |
|ConnectionString  <br/> |XSD: String  <br/> |Optional  <br/> |Die Verbindungszeichenfolge, die die Verbindung zu einer Datenquelle erforderlichen Parameter definiert.  <br/> |Werte des Typs xsd: String.  <br/> |
|FileName  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Name der Verbindungsdatei. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |Werte des Typs xsd: String.  <br/> |
|FriendlyName  <br/> |XSD: String  <br/> |Optional  <br/> |Ein Benutzer zur Verfügung gestellten Name für die Datenverbindung.  <br/> |Werte des Typs xsd: String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die ID für eine angegebene Verbindung, die innerhalb des Dokuments eindeutig von Visio zugewiesen.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Timeout  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die Wartezeit in Minuten beim Versuch, bevor der Versuch beendet eine Verbindung herzustellen.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

