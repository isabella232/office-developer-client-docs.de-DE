---
title: Zellenelement (Zeile "LineTo") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Enthält X- oder y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts.
ms.openlocfilehash: 284b315c156fed8ea3592d2c6825ff6b4bf4c279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796583"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="3b98f-103">Zellenelement (Zeile "LineTo") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3b98f-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="3b98f-104">Enthält X- oder y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="3b98f-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b98f-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3b98f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b98f-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3b98f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3b98f-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3b98f-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3b98f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3b98f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3b98f-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3b98f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3b98f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3b98f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3b98f-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="3b98f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3b98f-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="3b98f-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b98f-113">Definition</span><span class="sxs-lookup"><span data-stu-id="3b98f-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3b98f-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3b98f-114">Elements and attributes</span></span>

<span data-ttu-id="3b98f-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3b98f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3b98f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b98f-116">Parent elements</span></span>

|<span data-ttu-id="3b98f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b98f-117">**Element**</span></span>|<span data-ttu-id="3b98f-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3b98f-118">**Type**</span></span>|<span data-ttu-id="3b98f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b98f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b98f-120">Row-Element ("Geometry")</span><span class="sxs-lookup"><span data-stu-id="3b98f-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="3b98f-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="3b98f-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b98f-122">Enthält X- oder y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="3b98f-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3b98f-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b98f-123">Child elements</span></span>

|<span data-ttu-id="3b98f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b98f-124">**Element**</span></span>|<span data-ttu-id="3b98f-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3b98f-125">**Type**</span></span>|<span data-ttu-id="3b98f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b98f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b98f-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="3b98f-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3b98f-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="3b98f-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b98f-129">Gibt einen Verweis auf ein Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="3b98f-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3b98f-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b98f-130">Attributes</span></span>

|<span data-ttu-id="3b98f-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3b98f-131">**Attribute**</span></span>|<span data-ttu-id="3b98f-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3b98f-132">**Type**</span></span>|<span data-ttu-id="3b98f-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3b98f-133">**Required**</span></span>|<span data-ttu-id="3b98f-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b98f-134">**Description**</span></span>|<span data-ttu-id="3b98f-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3b98f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b98f-136">E</span><span class="sxs-lookup"><span data-stu-id="3b98f-136">E</span></span>  <br/> |<span data-ttu-id="3b98f-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3b98f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3b98f-138">Optional</span><span class="sxs-lookup"><span data-stu-id="3b98f-138">optional</span></span>  <br/> |<span data-ttu-id="3b98f-139">Gibt an, dass die Formel einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3b98f-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="3b98f-140">Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="3b98f-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="3b98f-141">Zeichenfolge mit einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="3b98f-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="3b98f-142">F</span><span class="sxs-lookup"><span data-stu-id="3b98f-142">F</span></span>  <br/> |<span data-ttu-id="3b98f-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3b98f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="3b98f-144">Optional</span><span class="sxs-lookup"><span data-stu-id="3b98f-144">optional</span></span>  <br/> | <span data-ttu-id="3b98f-145">Formel für das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b98f-145">Represents the element's formula.</span></span> <span data-ttu-id="3b98f-146">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="3b98f-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="3b98f-147">"(einige Formel)" Wenn die Formel lokal vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3b98f-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="3b98f-148">`No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b98f-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="3b98f-149">`Inh`Wenn die Formel geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="3b98f-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="3b98f-150">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="3b98f-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="3b98f-151">N</span><span class="sxs-lookup"><span data-stu-id="3b98f-151">N</span></span>  <br/> |<span data-ttu-id="3b98f-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3b98f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="3b98f-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3b98f-153">required</span></span>  <br/> |<span data-ttu-id="3b98f-154">Der Name der ShapeSheet-Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b98f-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="3b98f-155">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="3b98f-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="3b98f-156">Siehe Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="3b98f-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="3b98f-157">U</span><span class="sxs-lookup"><span data-stu-id="3b98f-157">U</span></span>  <br/> |<span data-ttu-id="3b98f-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3b98f-158">xsd:string</span></span>  <br/> |<span data-ttu-id="3b98f-159">Optional</span><span class="sxs-lookup"><span data-stu-id="3b98f-159">optional</span></span>  <br/> |<span data-ttu-id="3b98f-160">Stellt eine Einheit der Messung der Standardwert ist DL.</span><span class="sxs-lookup"><span data-stu-id="3b98f-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="3b98f-161">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="3b98f-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="3b98f-162">V</span><span class="sxs-lookup"><span data-stu-id="3b98f-162">V</span></span>  <br/> |<span data-ttu-id="3b98f-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3b98f-163">xsd:string</span></span>  <br/> |<span data-ttu-id="3b98f-164">Optional</span><span class="sxs-lookup"><span data-stu-id="3b98f-164">optional</span></span>  <br/> |<span data-ttu-id="3b98f-165">Den Wert der Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b98f-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="3b98f-166">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="3b98f-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b98f-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b98f-167">Remarks</span></span>

<span data-ttu-id="3b98f-168">Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3b98f-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="3b98f-169">Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="3b98f-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="3b98f-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3b98f-170">**Value**</span></span>|<span data-ttu-id="3b98f-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b98f-171">**Description**</span></span>|<span data-ttu-id="3b98f-172">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="3b98f-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b98f-173">X</span><span class="sxs-lookup"><span data-stu-id="3b98f-173">X</span></span>  <br/> |<span data-ttu-id="3b98f-174">Die X-Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="3b98f-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="3b98f-175">Zeile "LineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="3b98f-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="3b98f-176">v</span><span class="sxs-lookup"><span data-stu-id="3b98f-176">Y</span></span>  <br/> |<span data-ttu-id="3b98f-177">Die y-Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="3b98f-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="3b98f-178">Zeile "LineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="3b98f-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

