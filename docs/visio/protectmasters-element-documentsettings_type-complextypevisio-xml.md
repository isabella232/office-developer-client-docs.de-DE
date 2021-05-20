---
title: ProtectMasters-Element (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob der Benutzer am Erstellen, Bearbeiten oder Löschen von Masterformen gehindert wird. Der Benutzer kann unabhängig von dieser Einstellung immer noch neue Shapes aus einem Master-Shape erstellen.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540693"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a>ProtectMasters-Element (DocumentSettings_Type complexType) (Visio XML)

Gibt an, ob der Benutzer am Erstellen, Bearbeiten oder Löschen von Masterformen gehindert wird. Der Benutzer kann unabhängig von dieser Einstellung immer noch neue Shapes aus einem Master-Shape erstellen. 
  
Der Bereich der möglichen Werte für dieses Element ist entweder "0" oder "1". Der Wert "0" gibt an, dass Benutzer Masterformen erstellen, bearbeiten oder löschen können. Der Wert "1" gibt an, dass Benutzer Masterformen nicht erstellen, bearbeiten oder löschen können.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die Dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  

