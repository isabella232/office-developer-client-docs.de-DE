---
title: Trigger-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokumentteilen in einer Visio zu berechnen.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542905"
---
# <a name="trigger-element-visio-xml"></a>Trigger-Element (Visio XML)

Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokumentteilen in einer Visio zu berechnen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt Zellelemente an, die Informationen zur Definition einer Form bereitstellen.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Definiert die DocumentSheet-Struktur.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Repräsentiert eine in einem Dokument definierte Formatvorlage.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Zeichenblatt zugeordnet ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf eine Seite in der Zeichnung an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Name der Formel, die beim Aktivieren des Triggers aufgerufen werden soll.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise".  <br/> |Werte des xsd:string-Typs.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N-Attribut** dieses **Trigger-Elements** muss einer der begrenzten Werte sein, die den Triggeranweisungen entsprechen. In der folgenden Tabelle finden Sie  Informationen zu den Werten des N-Attributs, die für dieses **Trigger-Element zulässig** sind. 
  
|**Wert**|**Übergeordnetes Element**|**Beschreibung**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **HASCATEGORIES-Funktion** vorhanden ist.  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mit einer **BKGPAGENAME-Funktion** vorhanden ist  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn die Seite oder eine der enthaltenen Formen eine **RGB-Funktion** verwendet.  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DOCCREATION-Funktion vorhanden** ist.  <br/> |
|RecalcData1  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DATA1-Funktion** vorhanden ist.  <br/> |
|RecalcData2  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DATA2-Funktion** vorhanden ist.  <br/> |
|RecalcData3  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Form angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DATA3-Funktion** vorhanden ist.  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DOCLASTEDIT-Funktion** vorhanden ist.  <br/> |
|RecalcID  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **ID-Funktion** vorhanden ist.  <br/> |
|RecalcMasterName  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Form angezeigt wird, wenn ein teilübergreifender Verweis mit einer **MASTERNAME-Funktion** vorhanden ist.  <br/> |
|RecalcName  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **NAME-Funktion** vorhanden ist.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn die Seite oder eine der enthaltenden Formen über **eine NOW-** oder **EINE RAND-Funktion** verfügen.  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **PAGECOUNT-Funktion vorhanden** ist.  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Form angezeigt wird, wenn ein teilübergreifender Verweis mit einer **PAGENAME-Funktion** vorhanden ist.  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mit einer **PAGENUMBER-Funktion vorhanden** ist.  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Form angezeigt wird, wenn ein teilübergreifender Verweis mit einer **POINTALONGPATH-,** **PATHLENGTH-** oder **PATHSEGMENT-Funktion** vorhanden ist.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DOCLASTPRINT-Funktion vorhanden** ist.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **DOCLASTSAVE-Funktion** vorhanden ist.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **CATEGORY-,** **CREATOR-,** **DESCRIPTION-,** **KEYWORDS-,** **SUBJECT-** oder **TITLE-Funktion** vorhanden ist.  <br/> |
|RecalcType  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Form angezeigt wird, wenn ein teilübergreifender Verweis mit einer **TYPE-Funktion** vorhanden ist.  <br/> |
|RelChanged  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **CONTAINERMEMBERCOUNT-Funktion** vorhanden ist.  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mit einer **CONTAINERSHEETREF-Funktion** vorhanden ist.  <br/> |
|Pfad  <br/> |[Form](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mit einer **POINTALONGPATH-,** **PATHLENGTH-** oder **PATHSEGMENT-Funktion** vorhanden ist.  <br/> |
   

