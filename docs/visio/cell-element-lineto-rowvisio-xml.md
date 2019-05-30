---
title: Cell-Element (LineTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Enthält die x-oder y-Koordinaten des endscheitels eines geraden Linie-Segments.
ms.openlocfilehash: 4b1628549e659712a1c2e79ae0fbf53d594e18f9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539509"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="268c1-103">Cell-Element (LineTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="268c1-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="268c1-104">Enthält die x-oder y-Koordinaten des endscheitels eines geraden Linie-Segments.</span><span class="sxs-lookup"><span data-stu-id="268c1-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="268c1-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="268c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="268c1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="268c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="268c1-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="268c1-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="268c1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="268c1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="268c1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="268c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="268c1-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="268c1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="268c1-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="268c1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="268c1-112">Master #. XML, Seite #. XML</span><span class="sxs-lookup"><span data-stu-id="268c1-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="268c1-113">Definition</span><span class="sxs-lookup"><span data-stu-id="268c1-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="268c1-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="268c1-114">Elements and attributes</span></span>

<span data-ttu-id="268c1-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="268c1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="268c1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="268c1-116">Parent elements</span></span>

|<span data-ttu-id="268c1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="268c1-117">**Element**</span></span>|<span data-ttu-id="268c1-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="268c1-118">**Type**</span></span>|<span data-ttu-id="268c1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="268c1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="268c1-120">Row-Element (Geometry)</span><span class="sxs-lookup"><span data-stu-id="268c1-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="268c1-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="268c1-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="268c1-122">Enthält die x-oder y-Koordinaten des endscheitels eines geraden Linie-Segments.</span><span class="sxs-lookup"><span data-stu-id="268c1-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="268c1-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="268c1-123">Child elements</span></span>

|<span data-ttu-id="268c1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="268c1-124">**Element**</span></span>|<span data-ttu-id="268c1-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="268c1-125">**Type**</span></span>|<span data-ttu-id="268c1-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="268c1-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="268c1-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="268c1-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="268c1-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="268c1-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="268c1-129">Gibt einen Verweis auf ein Zeichenblatt an.</span><span class="sxs-lookup"><span data-stu-id="268c1-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="268c1-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="268c1-130">Attributes</span></span>

|<span data-ttu-id="268c1-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="268c1-131">**Attribute**</span></span>|<span data-ttu-id="268c1-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="268c1-132">**Type**</span></span>|<span data-ttu-id="268c1-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="268c1-133">**Required**</span></span>|<span data-ttu-id="268c1-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="268c1-134">**Description**</span></span>|<span data-ttu-id="268c1-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="268c1-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="268c1-136">E</span><span class="sxs-lookup"><span data-stu-id="268c1-136">E</span></span>  <br/> |<span data-ttu-id="268c1-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="268c1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="268c1-138">Optional</span><span class="sxs-lookup"><span data-stu-id="268c1-138">optional</span></span>  <br/> |<span data-ttu-id="268c1-139">Gibt an, dass die Formel zu einem Fehler ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="268c1-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="268c1-140">Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="268c1-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="268c1-141">Eine Fehler Meldungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="268c1-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="268c1-142">F</span><span class="sxs-lookup"><span data-stu-id="268c1-142">F</span></span>  <br/> |<span data-ttu-id="268c1-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="268c1-143">xsd:string</span></span>  <br/> |<span data-ttu-id="268c1-144">Optional</span><span class="sxs-lookup"><span data-stu-id="268c1-144">optional</span></span>  <br/> | <span data-ttu-id="268c1-145">Stellt die Formel des Elements dar.</span><span class="sxs-lookup"><span data-stu-id="268c1-145">Represents the element's formula.</span></span> <span data-ttu-id="268c1-146">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="268c1-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="268c1-147">"(eine Formel)", wenn die Formel lokal vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="268c1-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="268c1-148">`No Formula`Wenn die Formel lokal gelöscht oder blockiert wird</span><span class="sxs-lookup"><span data-stu-id="268c1-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="268c1-149">`Inh`, wenn die Formel vererbt wird.</span><span class="sxs-lookup"><span data-stu-id="268c1-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="268c1-150">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="268c1-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="268c1-151">N</span><span class="sxs-lookup"><span data-stu-id="268c1-151">N</span></span>  <br/> |<span data-ttu-id="268c1-152">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="268c1-152">xsd:string</span></span>  <br/> |<span data-ttu-id="268c1-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="268c1-153">required</span></span>  <br/> |<span data-ttu-id="268c1-154">Stellt den Namen der ShapeSheet-Zelle dar.</span><span class="sxs-lookup"><span data-stu-id="268c1-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="268c1-155">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="268c1-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="268c1-156">Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.</span><span class="sxs-lookup"><span data-stu-id="268c1-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="268c1-157">U</span><span class="sxs-lookup"><span data-stu-id="268c1-157">U</span></span>  <br/> |<span data-ttu-id="268c1-158">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="268c1-158">xsd:string</span></span>  <br/> |<span data-ttu-id="268c1-159">Optional</span><span class="sxs-lookup"><span data-stu-id="268c1-159">optional</span></span>  <br/> |<span data-ttu-id="268c1-160">Stellt eine Maßeinheit dar, bei der es sich bei der Standardeinstellung um DL handelt.</span><span class="sxs-lookup"><span data-stu-id="268c1-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="268c1-161">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="268c1-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="268c1-162">V</span><span class="sxs-lookup"><span data-stu-id="268c1-162">V</span></span>  <br/> |<span data-ttu-id="268c1-163">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="268c1-163">xsd:string</span></span>  <br/> |<span data-ttu-id="268c1-164">Optional</span><span class="sxs-lookup"><span data-stu-id="268c1-164">optional</span></span>  <br/> |<span data-ttu-id="268c1-165">Stellt den Wert der Zelle dar.</span><span class="sxs-lookup"><span data-stu-id="268c1-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="268c1-166">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="268c1-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="268c1-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="268c1-167">Remarks</span></span>

<span data-ttu-id="268c1-168">Das **N** -Attribut dieses **Cell** -Elements muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="268c1-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="268c1-169">In der folgenden Tabelle können Sie die Werte des **N** -Attributs bestimmen, die für dieses **Zellen** Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="268c1-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="268c1-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="268c1-170">**Value**</span></span>|<span data-ttu-id="268c1-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="268c1-171">**Description**</span></span>|<span data-ttu-id="268c1-172">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="268c1-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="268c1-173">X</span><span class="sxs-lookup"><span data-stu-id="268c1-173">X</span></span>  <br/> |<span data-ttu-id="268c1-174">Die x-Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="268c1-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="268c1-175">Zeile "LineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="268c1-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="268c1-176">v</span><span class="sxs-lookup"><span data-stu-id="268c1-176">Y</span></span>  <br/> |<span data-ttu-id="268c1-177">Die y-Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="268c1-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="268c1-178">Zeile "LineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="268c1-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

