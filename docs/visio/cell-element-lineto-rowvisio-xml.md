---
title: Cell-Element (LineTo-Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Enthält x-oder y-Koordinaten des Endpunkts eines geraden Linienabschnitts.
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318201"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="a6fab-103">Cell-Element (LineTo-Zeile) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a6fab-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="a6fab-104">Enthält x-oder y-Koordinaten des Endpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="a6fab-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6fab-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a6fab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6fab-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a6fab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a6fab-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a6fab-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a6fab-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a6fab-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a6fab-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a6fab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a6fab-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a6fab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a6fab-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="a6fab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a6fab-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="a6fab-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a6fab-113">Definition</span><span class="sxs-lookup"><span data-stu-id="a6fab-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a6fab-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a6fab-114">Elements and attributes</span></span>

<span data-ttu-id="a6fab-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a6fab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a6fab-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6fab-116">Parent elements</span></span>

|<span data-ttu-id="a6fab-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6fab-117">**Element**</span></span>|<span data-ttu-id="a6fab-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a6fab-118">**Type**</span></span>|<span data-ttu-id="a6fab-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6fab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a6fab-120">Row-Element (Geometry)</span><span class="sxs-lookup"><span data-stu-id="a6fab-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a6fab-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="a6fab-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a6fab-122">Enthält x-oder y-Koordinaten des Endpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="a6fab-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a6fab-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6fab-123">Child elements</span></span>

|<span data-ttu-id="a6fab-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6fab-124">**Element**</span></span>|<span data-ttu-id="a6fab-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a6fab-125">**Type**</span></span>|<span data-ttu-id="a6fab-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6fab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a6fab-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="a6fab-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a6fab-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a6fab-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a6fab-129">Gibt einen Verweis auf ein Zeichenblatt an.</span><span class="sxs-lookup"><span data-stu-id="a6fab-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a6fab-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6fab-130">Attributes</span></span>

|<span data-ttu-id="a6fab-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a6fab-131">**Attribute**</span></span>|<span data-ttu-id="a6fab-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a6fab-132">**Type**</span></span>|<span data-ttu-id="a6fab-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a6fab-133">**Required**</span></span>|<span data-ttu-id="a6fab-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6fab-134">**Description**</span></span>|<span data-ttu-id="a6fab-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a6fab-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a6fab-136">E</span><span class="sxs-lookup"><span data-stu-id="a6fab-136">E</span></span>  <br/> |<span data-ttu-id="a6fab-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fab-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a6fab-138">Optional</span><span class="sxs-lookup"><span data-stu-id="a6fab-138">optional</span></span>  <br/> |<span data-ttu-id="a6fab-139">Gibt an, dass die Formel zu einem Fehler ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="a6fab-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="a6fab-140">Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="a6fab-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="a6fab-141">Eine Fehlermeldungs-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a6fab-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="a6fab-142">F</span><span class="sxs-lookup"><span data-stu-id="a6fab-142">F</span></span>  <br/> |<span data-ttu-id="a6fab-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fab-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a6fab-144">Optional</span><span class="sxs-lookup"><span data-stu-id="a6fab-144">optional</span></span>  <br/> | <span data-ttu-id="a6fab-145">Stellt die Formel des Elements dar.</span><span class="sxs-lookup"><span data-stu-id="a6fab-145">Represents the element's formula.</span></span> <span data-ttu-id="a6fab-146">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="a6fab-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="a6fab-147">' (eine Formel) ', wenn die Formel lokal vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="a6fab-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="a6fab-148">`No Formula`Wenn die Formel lokal gelöscht oder gesperrt ist</span><span class="sxs-lookup"><span data-stu-id="a6fab-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="a6fab-149">`Inh`Wenn die Formel geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="a6fab-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="a6fab-150">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="a6fab-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="a6fab-151">N</span><span class="sxs-lookup"><span data-stu-id="a6fab-151">N</span></span>  <br/> |<span data-ttu-id="a6fab-152">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fab-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a6fab-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a6fab-153">required</span></span>  <br/> |<span data-ttu-id="a6fab-154">Stellt den Namen der ShapeSheet-Zelle dar.</span><span class="sxs-lookup"><span data-stu-id="a6fab-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="a6fab-155">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="a6fab-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="a6fab-156">Weitere Informationen finden Sie im Abschnitt "Hinweise" unten.</span><span class="sxs-lookup"><span data-stu-id="a6fab-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="a6fab-157">U</span><span class="sxs-lookup"><span data-stu-id="a6fab-157">U</span></span>  <br/> |<span data-ttu-id="a6fab-158">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fab-158">xsd:string</span></span>  <br/> |<span data-ttu-id="a6fab-159">Optional</span><span class="sxs-lookup"><span data-stu-id="a6fab-159">optional</span></span>  <br/> |<span data-ttu-id="a6fab-160">Stellt eine Maßeinheit dar der Standardwert ist DL.</span><span class="sxs-lookup"><span data-stu-id="a6fab-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="a6fab-161">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="a6fab-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="a6fab-162">V</span><span class="sxs-lookup"><span data-stu-id="a6fab-162">V</span></span>  <br/> |<span data-ttu-id="a6fab-163">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a6fab-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a6fab-164">Optional</span><span class="sxs-lookup"><span data-stu-id="a6fab-164">optional</span></span>  <br/> |<span data-ttu-id="a6fab-165">Stellt den Wert der Zelle dar.</span><span class="sxs-lookup"><span data-stu-id="a6fab-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="a6fab-166">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="a6fab-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6fab-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6fab-167">Remarks</span></span>

<span data-ttu-id="a6fab-168">Das **N** -Attribut dieses **Cell** -Elements muss einer einer begrenzten Menge von Werten sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a6fab-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="a6fab-169">In der nachstehenden Tabelle finden Sie die Werte des **N** -Attributs, die für dieses **Cell** -Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a6fab-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="a6fab-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a6fab-170">**Value**</span></span>|<span data-ttu-id="a6fab-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6fab-171">**Description**</span></span>|<span data-ttu-id="a6fab-172">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="a6fab-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6fab-173">X</span><span class="sxs-lookup"><span data-stu-id="a6fab-173">X</span></span>  <br/> |<span data-ttu-id="a6fab-174">Die x-Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="a6fab-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="a6fab-175">Zeile "LineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="a6fab-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="a6fab-176">v</span><span class="sxs-lookup"><span data-stu-id="a6fab-176">Y</span></span>  <br/> |<span data-ttu-id="a6fab-177">Die y-Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="a6fab-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="a6fab-178">Zeile "LineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="a6fab-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

