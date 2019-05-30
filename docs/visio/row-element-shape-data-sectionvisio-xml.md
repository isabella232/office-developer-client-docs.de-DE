---
title: Row-Element (Shape Data Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Gibt eine Shape-Dateneingabe für das Zuordnen von Daten zu einer Form an.
ms.openlocfilehash: 4c5644aa2088dcaf3be81ea9aeaa549c911a31f6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538270"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="ddcc3-103">Row-Element (Shape Data Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ddcc3-103">Row element (Shape Data Section) (Visio XML)</span></span>

<span data-ttu-id="ddcc3-104">Gibt eine Shape-Dateneingabe für das Zuordnen von Daten zu einer Form an.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddcc3-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ddcc3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddcc3-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ddcc3-107">Shape-daten_type</span><span class="sxs-lookup"><span data-stu-id="ddcc3-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ddcc3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ddcc3-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ddcc3-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ddcc3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ddcc3-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ddcc3-112">Master #. XML, Seite #. XML</span><span class="sxs-lookup"><span data-stu-id="ddcc3-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ddcc3-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ddcc3-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ddcc3-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ddcc3-114">Elements and attributes</span></span>

<span data-ttu-id="ddcc3-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ddcc3-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddcc3-116">Parent elements</span></span>

|<span data-ttu-id="ddcc3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-117">**Element**</span></span>|<span data-ttu-id="ddcc3-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-118">**Type**</span></span>|<span data-ttu-id="ddcc3-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddcc3-120">Section</span><span class="sxs-lookup"><span data-stu-id="ddcc3-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ddcc3-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ddcc3-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ddcc3-122">Gibt eine Shape-Dateneingabe für das Zuordnen von Daten zu einer Form an.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ddcc3-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ddcc3-123">Child elements</span></span>

|<span data-ttu-id="ddcc3-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-124">**Element**</span></span>|<span data-ttu-id="ddcc3-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-125">**Type**</span></span>|<span data-ttu-id="ddcc3-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddcc3-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ddcc3-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ddcc3-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ddcc3-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ddcc3-129">Gibt eine Eigenschaft der Shape-Daten an.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ddcc3-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="ddcc3-130">Attributes</span></span>

|<span data-ttu-id="ddcc3-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-131">**Attribute**</span></span>|<span data-ttu-id="ddcc3-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-132">**Type**</span></span>|<span data-ttu-id="ddcc3-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-133">**Required**</span></span>|<span data-ttu-id="ddcc3-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-134">**Description**</span></span>|<span data-ttu-id="ddcc3-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ddcc3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ddcc3-136">Del</span><span class="sxs-lookup"><span data-stu-id="ddcc3-136">Del</span></span>  <br/> |<span data-ttu-id="ddcc3-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ddcc3-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ddcc3-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ddcc3-138">optional</span></span>  <br/> |<span data-ttu-id="ddcc3-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="ddcc3-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ddcc3-141">IX</span><span class="sxs-lookup"><span data-stu-id="ddcc3-141">IX</span></span>  <br/> |<span data-ttu-id="ddcc3-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ddcc3-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ddcc3-143">Optional</span><span class="sxs-lookup"><span data-stu-id="ddcc3-143">optional</span></span>  <br/> |<span data-ttu-id="ddcc3-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="ddcc3-145">Es sollte eindeutigen und größer sein als andere Bezeichner im gleichen Abschnitt. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="ddcc3-146">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ddcc3-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ddcc3-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="ddcc3-148">LocalName</span></span>  <br/> |<span data-ttu-id="ddcc3-149">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ddcc3-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ddcc3-150">Optional</span><span class="sxs-lookup"><span data-stu-id="ddcc3-150">optional</span></span>  <br/> |<span data-ttu-id="ddcc3-151">Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="ddcc3-152">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ddcc3-153">N</span><span class="sxs-lookup"><span data-stu-id="ddcc3-153">N</span></span>  <br/> |<span data-ttu-id="ddcc3-154">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ddcc3-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ddcc3-155">Optional</span><span class="sxs-lookup"><span data-stu-id="ddcc3-155">optional</span></span>  <br/> |<span data-ttu-id="ddcc3-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="ddcc3-157">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ddcc3-158">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ddcc3-159">T</span><span class="sxs-lookup"><span data-stu-id="ddcc3-159">T</span></span>  <br/> |<span data-ttu-id="ddcc3-160">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ddcc3-160">xsd:string</span></span>  <br/> |<span data-ttu-id="ddcc3-161">Optional</span><span class="sxs-lookup"><span data-stu-id="ddcc3-161">optional</span></span>  <br/> |<span data-ttu-id="ddcc3-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt wird und in der Geometrie Visualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="ddcc3-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="ddcc3-164">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ddcc3-164">Values of the xsd:string type.</span></span>  <br/> |
   

