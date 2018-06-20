---
title: RefBy-Element (Trigger_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf eine Seite in der Zeichnung.
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797783"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a>RefBy-Element (Trigger_Type ComplexType) ("Visio XML")

Gibt einen Verweis auf eine Seite in der Zeichnung.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> ||
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Trigger](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.  <br/> |
|[Trigger](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.  <br/> |
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt das ID-Attribut des einer Seite in der Zeichnung.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|T  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des Typs xsd: String.  <br/> |
   

