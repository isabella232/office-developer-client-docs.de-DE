---
title: Trigger-Element (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokument Teilen in einer Visio-Datei neu zu berechnen.
ms.openlocfilehash: a590ec1f9c19270f75d4d9e77804c0a7b45157b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280850"
---
# <a name="trigger-element-visio-xml"></a>Trigger-Element (' Visio XML ')

Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokument Teilen in einer Visio-Datei neu zu berechnen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt Zellen Elemente an, die Informationen für die Definition einer Form bereitstellen.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Definiert die DocumentSheet-Struktur.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Repräsentiert eine in einem Dokument definierte Formatvorlage.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Zeichenblatt zugeordnet ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt eine Referenz-Toa-Seite in der Zeichnung an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Der Name der Formel, die aufgerufen werden soll, wenn der Trigger aktiviert wird.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise".  <br/> |Werte des XSD: String-Typs.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses **Trigger** -Elements muss einer einer begrenzten Menge von Werten entsprechen, die den Trigger-Anweisungen entspricht. In der nachstehenden Tabelle finden Sie die Werte des **N** -Attributs, die für dieses **Trigger** -Element zulässig sind. 
  
|**Wert**|**Übergeordnetes Element**|**Beschreibung**|
|:-----|:-----|:-----|
|Category-of  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **HASCATEGORIES** -Funktion vorhanden ist.  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein übergreifender Verweis mit einer **BKGPAGENAME** -Funktion vorhanden ist  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn die Seite oder eine der enthaltenen Shapes eine **RGB** -Funktion verwendet.  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn eine übergreifende Referenz mit einer **DOCCREATION** -Funktion vorhanden ist.  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **data1** -Funktion vorhanden ist.  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **data2** -Funktion vorhanden ist.  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **data3** -Funktion vorhanden ist.  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn eine übergreifende Referenz mit einer **DOCLASTEDIT** -Funktion vorhanden ist.  <br/> |
|Neuberechnung  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **ID-** Funktion vorhanden ist.  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende **** Referenz mit einer Mastername-Funktion vorhanden ist.  <br/> |
|Recalcname  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **Name** -Funktion vorhanden ist.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn die Seite oder eine der enthaltenen Formen eine **Now** -oder eine **Rand** -Funktion aufweisen.  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn eine übergreifende Referenz mit einer **PageCount** -Funktion vorhanden ist.  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein übergreifender **** Verweis mithilfe einer pagename-Funktion vorhanden ist.  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein übergreifender Verweis mit einer **PageNumber** -Funktion vorhanden ist.  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **POINTALONGPATH**-, **PATHLENGTH**-oder **PATHSEGMENT** -Funktion vorhanden ist.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn eine übergreifende Referenz mit einer **DOCLASTPRINT** -Funktion vorhanden ist.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn eine übergreifende Referenz mit einer **DOCLASTSAVE** -Funktion vorhanden ist.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn eine übergreifende Referenz mit einer **Category**-, **Creator**-, **Description**-, **Schlüsselwort**-, **Subject**-oder **Title** -Funktion vorhanden ist.  <br/> |
|Recalctype  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **Type** -Funktion vorhanden ist.  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn eine übergreifende Referenz mit einer **CONTAINERMEMBERCOUNT** -Funktion vorhanden ist.  <br/> |
|"Zorderchanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein übergreifender Verweis mit einer **CONTAINERSHEETREF** -Funktion vorhanden ist.  <br/> |
|Pfad  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn eine übergreifende Referenz mit einer **POINTALONGPATH**-, **PATHLENGTH**-oder **PATHSEGMENT** -Funktion vorhanden ist.  <br/> |
   

