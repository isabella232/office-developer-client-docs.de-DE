---
title: ProtectMasters-Element (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob der Benutzer Master-Shapes nicht erstellen, bearbeiten oder löschen kann. Der Benutzer kann weiterhin neue Shapes aus einem Master-Shape erstellen, unabhängig von dieser Einstellung.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314819"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>ProtectMasters-Element (DocumentSettings_Type complexType) (' Visio XML ')

Gibt an, ob der Benutzer Master-Shapes nicht erstellen, bearbeiten oder löschen kann. Der Benutzer kann weiterhin neue Shapes aus einem Master-Shape erstellen, unabhängig von dieser Einstellung. 
  
Der mögliche Wert für dieses Element ist entweder "0" oder "1". Der Wert "0" gibt an, dass Benutzer Master-Shapes erstellen, bearbeiten oder löschen können. Der Wert "1" gibt an, dass Benutzer keine Master-Shapes erstellen, bearbeiten oder löschen können.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die Dokumenteinstellungen angeben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

Keine.
  

