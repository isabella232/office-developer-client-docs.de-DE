---
title: Row-Element (Abschnitt "Shape Data") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Gibt einen Shapedateneintrag zum Zuordnen von Daten zu einer Form an.
ms.openlocfilehash: 4c5644aa2088dcaf3be81ea9aeaa549c911a31f6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538270"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="aa101-103">Row-Element (Abschnitt "Shape Data") (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aa101-103">Row element (Shape Data Section) (Visio XML)</span></span>

<span data-ttu-id="aa101-104">Gibt einen Shapedateneintrag zum Zuordnen von Daten zu einer Form an.</span><span class="sxs-lookup"><span data-stu-id="aa101-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa101-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="aa101-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa101-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="aa101-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aa101-107">Shape-Data_Type</span><span class="sxs-lookup"><span data-stu-id="aa101-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aa101-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aa101-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aa101-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="aa101-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aa101-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="aa101-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aa101-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="aa101-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aa101-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="aa101-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aa101-113">Definition</span><span class="sxs-lookup"><span data-stu-id="aa101-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aa101-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="aa101-114">Elements and attributes</span></span>

<span data-ttu-id="aa101-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="aa101-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aa101-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa101-116">Parent elements</span></span>

|<span data-ttu-id="aa101-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa101-117">**Element**</span></span>|<span data-ttu-id="aa101-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa101-118">**Type**</span></span>|<span data-ttu-id="aa101-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa101-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa101-120">Section</span><span class="sxs-lookup"><span data-stu-id="aa101-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa101-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="aa101-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aa101-122">Gibt einen Shapedateneintrag zum Zuordnen von Daten zu einer Form an.</span><span class="sxs-lookup"><span data-stu-id="aa101-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aa101-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa101-123">Child elements</span></span>

|<span data-ttu-id="aa101-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa101-124">**Element**</span></span>|<span data-ttu-id="aa101-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa101-125">**Type**</span></span>|<span data-ttu-id="aa101-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa101-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa101-127">Cell</span><span class="sxs-lookup"><span data-stu-id="aa101-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="aa101-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="aa101-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aa101-129">Gibt eine Eigenschaft der Shapedaten an.</span><span class="sxs-lookup"><span data-stu-id="aa101-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aa101-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa101-130">Attributes</span></span>

|<span data-ttu-id="aa101-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aa101-131">**Attribute**</span></span>|<span data-ttu-id="aa101-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa101-132">**Type**</span></span>|<span data-ttu-id="aa101-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="aa101-133">**Required**</span></span>|<span data-ttu-id="aa101-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa101-134">**Description**</span></span>|<span data-ttu-id="aa101-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="aa101-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aa101-136">Del</span><span class="sxs-lookup"><span data-stu-id="aa101-136">Del</span></span>  <br/> |<span data-ttu-id="aa101-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aa101-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa101-138">Optional</span><span class="sxs-lookup"><span data-stu-id="aa101-138">optional</span></span>  <br/> |<span data-ttu-id="aa101-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="aa101-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="aa101-140">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aa101-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa101-141">IX</span><span class="sxs-lookup"><span data-stu-id="aa101-141">IX</span></span>  <br/> |<span data-ttu-id="aa101-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aa101-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aa101-143">Optional</span><span class="sxs-lookup"><span data-stu-id="aa101-143">optional</span></span>  <br/> |<span data-ttu-id="aa101-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="aa101-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="aa101-145">Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa101-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="aa101-146">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aa101-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="aa101-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa101-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aa101-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="aa101-148">LocalName</span></span>  <br/> |<span data-ttu-id="aa101-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa101-149">xsd:string</span></span>  <br/> |<span data-ttu-id="aa101-150">Optional</span><span class="sxs-lookup"><span data-stu-id="aa101-150">optional</span></span>  <br/> |<span data-ttu-id="aa101-151">Gibt den eindeutigen sprachabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="aa101-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="aa101-152">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa101-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa101-153">N</span><span class="sxs-lookup"><span data-stu-id="aa101-153">N</span></span>  <br/> |<span data-ttu-id="aa101-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa101-154">xsd:string</span></span>  <br/> |<span data-ttu-id="aa101-155">Optional</span><span class="sxs-lookup"><span data-stu-id="aa101-155">optional</span></span>  <br/> |<span data-ttu-id="aa101-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa101-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="aa101-157">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aa101-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="aa101-158">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa101-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa101-159">T</span><span class="sxs-lookup"><span data-stu-id="aa101-159">T</span></span>  <br/> |<span data-ttu-id="aa101-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aa101-160">xsd:string</span></span>  <br/> |<span data-ttu-id="aa101-161">Optional</span><span class="sxs-lookup"><span data-stu-id="aa101-161">optional</span></span>  <br/> |<span data-ttu-id="aa101-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa101-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="aa101-163">Das T-Attribut wird nur für den Abschnitt Geometry verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa101-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="aa101-164">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="aa101-164">Values of the xsd:string type.</span></span>  <br/> |
   

