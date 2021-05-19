---
title: Row-Element (Connection Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Enthält die X- oder Y-Koordinaten, horizontale und vertikale Richtung und gibt einen einzelnen Verbindungspunkt für eine Form ein.
ms.openlocfilehash: eb32030e89d3ac77adfdc64e2d20a5fb954dbb53
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541764"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="f041a-103">Row-Element (Connection Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f041a-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="f041a-104">Enthält die X- oder Y-Koordinaten, horizontale und vertikale Richtung und gibt einen einzelnen Verbindungspunkt für eine Form ein.</span><span class="sxs-lookup"><span data-stu-id="f041a-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f041a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f041a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f041a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f041a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f041a-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="f041a-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f041a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f041a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f041a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f041a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f041a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f041a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f041a-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="f041a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f041a-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="f041a-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f041a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="f041a-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f041a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f041a-114">Elements and attributes</span></span>

<span data-ttu-id="f041a-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f041a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f041a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f041a-116">Parent elements</span></span>

|<span data-ttu-id="f041a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f041a-117">**Element**</span></span>|<span data-ttu-id="f041a-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f041a-118">**Type**</span></span>|<span data-ttu-id="f041a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f041a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f041a-120">Section</span><span class="sxs-lookup"><span data-stu-id="f041a-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f041a-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="f041a-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f041a-122">Enthält die X- oder Y-Koordinaten, horizontale und vertikale Richtung und gibt einen einzelnen Verbindungspunkt für eine Form ein.</span><span class="sxs-lookup"><span data-stu-id="f041a-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f041a-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f041a-123">Child elements</span></span>

|<span data-ttu-id="f041a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f041a-124">**Element**</span></span>|<span data-ttu-id="f041a-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f041a-125">**Type**</span></span>|<span data-ttu-id="f041a-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f041a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f041a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="f041a-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="f041a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f041a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f041a-129">Gibt eine einzelne Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="f041a-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f041a-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="f041a-130">Attributes</span></span>

|<span data-ttu-id="f041a-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f041a-131">**Attribute**</span></span>|<span data-ttu-id="f041a-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f041a-132">**Type**</span></span>|<span data-ttu-id="f041a-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f041a-133">**Required**</span></span>|<span data-ttu-id="f041a-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f041a-134">**Description**</span></span>|<span data-ttu-id="f041a-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f041a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f041a-136">Del</span><span class="sxs-lookup"><span data-stu-id="f041a-136">Del</span></span>  <br/> |<span data-ttu-id="f041a-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f041a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f041a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="f041a-138">optional</span></span>  <br/> |<span data-ttu-id="f041a-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="f041a-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="f041a-140">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f041a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f041a-141">IX</span><span class="sxs-lookup"><span data-stu-id="f041a-141">IX</span></span>  <br/> |<span data-ttu-id="f041a-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f041a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f041a-143">Optional</span><span class="sxs-lookup"><span data-stu-id="f041a-143">optional</span></span>  <br/> |<span data-ttu-id="f041a-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="f041a-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="f041a-145">Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="f041a-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="f041a-146">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f041a-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f041a-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f041a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f041a-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="f041a-148">LocalName</span></span>  <br/> |<span data-ttu-id="f041a-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f041a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="f041a-150">Optional</span><span class="sxs-lookup"><span data-stu-id="f041a-150">optional</span></span>  <br/> |<span data-ttu-id="f041a-151">Gibt den eindeutigen sprachabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="f041a-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="f041a-152">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="f041a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f041a-153">N</span><span class="sxs-lookup"><span data-stu-id="f041a-153">N</span></span>  <br/> |<span data-ttu-id="f041a-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f041a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="f041a-155">Optional</span><span class="sxs-lookup"><span data-stu-id="f041a-155">optional</span></span>  <br/> |<span data-ttu-id="f041a-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="f041a-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="f041a-157">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f041a-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f041a-158">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="f041a-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f041a-159">T</span><span class="sxs-lookup"><span data-stu-id="f041a-159">T</span></span>  <br/> |<span data-ttu-id="f041a-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f041a-160">xsd:string</span></span>  <br/> |<span data-ttu-id="f041a-161">Optional</span><span class="sxs-lookup"><span data-stu-id="f041a-161">optional</span></span>  <br/> |<span data-ttu-id="f041a-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f041a-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="f041a-163">Das T-Attribut wird nur für den Abschnitt Geometry verwendet.</span><span class="sxs-lookup"><span data-stu-id="f041a-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="f041a-164">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="f041a-164">Values of the xsd:string type.</span></span>  <br/> |
   

