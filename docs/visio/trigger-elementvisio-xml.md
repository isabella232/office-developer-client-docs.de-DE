---
title: Trigger-Element (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokumentteilen in einer Visio Datei neu zu berechnen.
ms.openlocfilehash: c6223107182862df0772316dab2218dbf6180fae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549454"
---
# <a name="trigger-element-visio-xml"></a>Trigger-Element (Visio XML)

Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokumentteilen in einer Visio Datei neu zu berechnen.
  
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt Zellenelemente an, die Informationen für die Definition eines Shapes bereitstellen.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Definiert die DocumentSheet-Struktur.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Repräsentiert eine in einem Dokument definierte Formatvorlage.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Zeichenblatt zugeordnet ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Name der Formel, die aufgerufen werden soll, wenn der Trigger aktiviert wird.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise".  <br/> |Werte des Typs "xsd:string".  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **N-Attribut** dieses **Trigger-Elements** muss einer der begrenzten Werte sein, die Triggeranweisungen entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Trigger-Element** zulässig sind. 
  
|**Wert**|**Übergeordnetes Element**|**Beschreibung**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **HASCATEGORIES-Funktion** vorhanden ist.  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **BKGPAGENAME-Funktion** vorhanden ist  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Zeichenblatt angezeigt wird, wenn das Zeichenblatt oder eine seiner enthaltenen Formen eine **RGB-Funktion** verwendet.  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DOCCREATION-Funktion** vorhanden ist.  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DATA1-Funktion** vorhanden ist.  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DATA2-Funktion** vorhanden ist.  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DATA3-Funktion** vorhanden ist.  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DOCLASTEDIT-Funktion** vorhanden ist.  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **ID-Funktion** vorhanden ist.  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **MASTERNAME-Funktion** vorhanden ist.  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **NAME-Funktion** vorhanden ist.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Zeichenblatt angezeigt wird, wenn das Zeichenblatt oder eines der enthaltenden Shapes eine **NOW-** oder EINE **RAND-Funktion** aufweist.  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **PAGECOUNT-Funktion** vorhanden ist.  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **PAGENAME-Funktion** vorhanden ist.  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **PAGENUMBER-Funktion** vorhanden ist.  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mit einer **POINTALONGPATH-,** **PATHLENGTH-** oder **PATHSEGMENT-Funktion** vorhanden ist.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DOCLASTPRINT-Funktion** vorhanden ist.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **DOCLASTSAVE-Funktion** vorhanden ist.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein teilübergreifender Verweis mit einer **CATEGORY-,** **CREATOR-,** **DESCRIPTION-,** **KEYWORDS-,** **SUBJECT-** oder **TITLE-Funktion** vorhanden ist.  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **TYPE-Funktion** vorhanden ist.  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Shape angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **CONTAINERMEMBERCOUNT-Funktion** vorhanden ist.  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **CONTAINERSHEETREF-Funktion** vorhanden ist.  <br/> |
|Pfad  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein teilübergreifender Verweis mithilfe einer **POINTALONGPATH-,** **PATHLENGTH-** oder **PATHSEGMENT-Funktion** vorhanden ist.  <br/> |
   

