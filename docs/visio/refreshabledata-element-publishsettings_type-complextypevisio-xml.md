---
title: RefreshableData-Element (PublishSettings_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: Gibt an, ob ein Recordset-Objekt aktualisierbare mithilfe von Visio Services in Microsoft SharePoint Server 2013.
ms.openlocfilehash: b402e2c9d65bf868c0ac33c782b87857ab6aed75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384872"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a>RefreshableData-Element (PublishSettings_Type ComplexType) ("Visio XML")

Gibt an, ob ein Recordset-Objekt aktualisierbare mithilfe von Visio Services in Microsoft SharePoint Server 2013.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PublishSettings](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |Gibt die Einstellungen, die verwendet werden, wenn das Diagramm mit Visio Services geöffnet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Der Bezeichner eines Recordset-Objekts.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

