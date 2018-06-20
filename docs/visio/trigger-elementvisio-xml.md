---
title: Trigger-Element ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.
ms.openlocfilehash: 909fff3ccec176cd3ce327fc208c176a68764fe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798321"
---
# <a name="trigger-element-visio-xml"></a>Trigger-Element ("Visio XML")

Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |# .xml Master, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt die Zellenelemente, die Informationen für die Definition eines Shapes enthalten.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Definiert die DocumentSheet-Struktur.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Repräsentiert eine in einem Dokument definierte Formatvorlage.  <br/> |
|[PageSheet (Master_Type ComplexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts das Master-Shape zugeordnet.  <br/> |
|[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichnungsfensters Zeichenblatt zugeordnet.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt eine Referenzseite Toa in der Zeichnung.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Name der die Formel, die aufgerufen werden, wenn der Trigger aktiviert ist.  <br/> Finden Sie unter "Hinweise".  <br/> |Werte des Typs xsd: String.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N** -Attribut des dieser **Trigger** -Element muss eine der eine begrenzte Auswahl von Werten sein, die Trigger Anweisungen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Trigger** -Element zulässig sind. 
  
|**Wert**|**Übergeordnetes Element**|**Beschreibung**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer Funktion **HASCATEGORIES** vorhanden ist.  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **BKGPAGENAME-** Funktion vorhanden ist.  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn die Seite oder eines seiner enthaltenen Shapes **RGB** -Funktion verwendet.  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DOCCREATION-** Funktion vorhanden ist.  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DATA1** -Funktion vorhanden ist.  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DATA2** -Funktion vorhanden ist.  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DATA3** -Funktion vorhanden ist.  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DOCLASTEDIT** -Funktion vorhanden ist.  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer Funktion **ID** vorhanden ist.  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **MASTERNAME** -Funktion vorhanden ist.  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer Funktion **Namen** vorhanden ist.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn die Seite oder eines der enthaltenden Shapes einer **nun** oder **RAND** -Funktion verfügen.  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **PAGECOUNT** -Funktion vorhanden ist.  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **PAGENAME** -Funktion vorhanden ist.  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein **PAGENUMBER** -Funktion mit Cross-Teil Verweis vorhanden ist.  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf ein Shape, wenn ein Cross-Teil Verweis mithilfe einer Funktion **POINTALONGPATH**, **PATHLENGTH**oder **PATHSEGMENT** angezeigt wird, ist vorhanden.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DOCLASTPRINT-** Funktion vorhanden ist.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **DOCLASTSAVE-** Funktion vorhanden ist.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Ein Trigger, der in einem Dokument, wenn ein Cross-Teil Verweis mithilfe einer Funktion **Kategorie**, **CREATOR**, **Beschreibung**, **SCHLÜSSELWÖRTER**, **Betreff**oder **Titel** angezeigt wird, ist vorhanden.  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer Funktion **Typ** vorhanden ist.  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einem Shape angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **CONTAINERMEMBERCOUNT** -Funktion vorhanden ist.  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type ComplexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite angezeigt wird, wenn ein Cross-Teil Verweis mithilfe einer **CONTAINERSHEETREF** -Funktion vorhanden ist.  <br/> |
|Pfad  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Ein Trigger, der auf einer Seite, wenn ein Cross-Teil Verweis mithilfe einer Funktion **POINTALONGPATH**, **PATHLENGTH**oder **PATHSEGMENT** angezeigt wird, ist vorhanden.  <br/> |
   

