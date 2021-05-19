---
title: Row-Element (Abschnitt "Controls") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Enthält die Zellen für ein bestimmtes Steuerelementhandle, das für ein Shape definiert ist.
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541743"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="66323-103">Row-Element (Abschnitt "Controls") (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="66323-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="66323-104">Enthält die Zellen für ein bestimmtes Steuerelementhandle, das für ein Shape definiert ist.</span><span class="sxs-lookup"><span data-stu-id="66323-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66323-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66323-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66323-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="66323-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66323-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="66323-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66323-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66323-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66323-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="66323-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66323-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66323-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66323-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="66323-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66323-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="66323-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66323-113">Definition</span><span class="sxs-lookup"><span data-stu-id="66323-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66323-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="66323-114">Elements and attributes</span></span>

<span data-ttu-id="66323-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="66323-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66323-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66323-116">Parent elements</span></span>

|<span data-ttu-id="66323-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="66323-117">**Element**</span></span>|<span data-ttu-id="66323-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="66323-118">**Type**</span></span>|<span data-ttu-id="66323-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66323-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66323-120">Section</span><span class="sxs-lookup"><span data-stu-id="66323-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66323-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="66323-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66323-122">Enthält die Zellen für ein bestimmtes Steuerelementhandle, das für ein Shape definiert ist.</span><span class="sxs-lookup"><span data-stu-id="66323-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66323-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66323-123">Child elements</span></span>

|<span data-ttu-id="66323-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="66323-124">**Element**</span></span>|<span data-ttu-id="66323-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="66323-125">**Type**</span></span>|<span data-ttu-id="66323-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66323-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66323-127">Cell</span><span class="sxs-lookup"><span data-stu-id="66323-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="66323-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="66323-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66323-129">Enthält eine Eigenschaft für ein bestimmtes Steuerelementhandle, das für eine Form definiert ist.</span><span class="sxs-lookup"><span data-stu-id="66323-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="66323-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="66323-130">Attributes</span></span>

|<span data-ttu-id="66323-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="66323-131">**Attribute**</span></span>|<span data-ttu-id="66323-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="66323-132">**Type**</span></span>|<span data-ttu-id="66323-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="66323-133">**Required**</span></span>|<span data-ttu-id="66323-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66323-134">**Description**</span></span>|<span data-ttu-id="66323-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="66323-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66323-136">Del</span><span class="sxs-lookup"><span data-stu-id="66323-136">Del</span></span>  <br/> |<span data-ttu-id="66323-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="66323-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="66323-138">Optional</span><span class="sxs-lookup"><span data-stu-id="66323-138">optional</span></span>  <br/> |<span data-ttu-id="66323-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="66323-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="66323-140">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="66323-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="66323-141">IX</span><span class="sxs-lookup"><span data-stu-id="66323-141">IX</span></span>  <br/> |<span data-ttu-id="66323-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="66323-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="66323-143">Optional</span><span class="sxs-lookup"><span data-stu-id="66323-143">optional</span></span>  <br/> |<span data-ttu-id="66323-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="66323-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="66323-145">Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="66323-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="66323-146">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="66323-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="66323-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="66323-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="66323-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="66323-148">LocalName</span></span>  <br/> |<span data-ttu-id="66323-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="66323-149">xsd:string</span></span>  <br/> |<span data-ttu-id="66323-150">Optional</span><span class="sxs-lookup"><span data-stu-id="66323-150">optional</span></span>  <br/> |<span data-ttu-id="66323-151">Gibt den eindeutigen sprachabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="66323-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="66323-152">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="66323-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="66323-153">N</span><span class="sxs-lookup"><span data-stu-id="66323-153">N</span></span>  <br/> |<span data-ttu-id="66323-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="66323-154">xsd:string</span></span>  <br/> |<span data-ttu-id="66323-155">Optional</span><span class="sxs-lookup"><span data-stu-id="66323-155">optional</span></span>  <br/> |<span data-ttu-id="66323-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="66323-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="66323-157">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="66323-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="66323-158">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="66323-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="66323-159">T</span><span class="sxs-lookup"><span data-stu-id="66323-159">T</span></span>  <br/> |<span data-ttu-id="66323-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="66323-160">xsd:string</span></span>  <br/> |<span data-ttu-id="66323-161">Optional</span><span class="sxs-lookup"><span data-stu-id="66323-161">optional</span></span>  <br/> |<span data-ttu-id="66323-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66323-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="66323-163">Das T-Attribut wird nur für den Abschnitt Geometry verwendet.</span><span class="sxs-lookup"><span data-stu-id="66323-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="66323-164">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="66323-164">Values of the xsd:string type.</span></span>  <br/> |
   

