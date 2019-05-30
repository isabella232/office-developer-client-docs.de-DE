---
title: Row-Element (Layer section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Enthält Elemente, die eine einzelne Ebene und deren Eigenschaften für eine Seite definieren.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540862"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="c0b04-103">Row-Element (Layer section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c0b04-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="c0b04-104">Enthält Elemente, die eine einzelne Ebene und deren Eigenschaften für eine Seite definieren.</span><span class="sxs-lookup"><span data-stu-id="c0b04-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0b04-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0b04-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0b04-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c0b04-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c0b04-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="c0b04-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c0b04-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c0b04-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c0b04-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c0b04-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c0b04-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c0b04-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c0b04-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="c0b04-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c0b04-112">Masters. XML, Pages. XML</span><span class="sxs-lookup"><span data-stu-id="c0b04-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c0b04-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c0b04-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c0b04-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c0b04-114">Elements and attributes</span></span>

<span data-ttu-id="c0b04-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c0b04-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c0b04-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0b04-116">Parent elements</span></span>

|<span data-ttu-id="c0b04-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0b04-117">**Element**</span></span>|<span data-ttu-id="c0b04-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0b04-118">**Type**</span></span>|<span data-ttu-id="c0b04-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0b04-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0b04-120">Section</span><span class="sxs-lookup"><span data-stu-id="c0b04-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c0b04-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c0b04-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c0b04-122">Enthält Elemente, die eine einzelne Ebene und deren Eigenschaften für eine Seite definieren.</span><span class="sxs-lookup"><span data-stu-id="c0b04-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c0b04-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0b04-123">Child elements</span></span>

|<span data-ttu-id="c0b04-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0b04-124">**Element**</span></span>|<span data-ttu-id="c0b04-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0b04-125">**Type**</span></span>|<span data-ttu-id="c0b04-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0b04-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0b04-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c0b04-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c0b04-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c0b04-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c0b04-129">Gibt eine Eigenschaft für einen Layer oder seine Eigenschaften für eine Seite an.</span><span class="sxs-lookup"><span data-stu-id="c0b04-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c0b04-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0b04-130">Attributes</span></span>

|<span data-ttu-id="c0b04-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c0b04-131">**Attribute**</span></span>|<span data-ttu-id="c0b04-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0b04-132">**Type**</span></span>|<span data-ttu-id="c0b04-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c0b04-133">**Required**</span></span>|<span data-ttu-id="c0b04-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0b04-134">**Description**</span></span>|<span data-ttu-id="c0b04-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c0b04-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c0b04-136">Del</span><span class="sxs-lookup"><span data-stu-id="c0b04-136">Del</span></span>  <br/> |<span data-ttu-id="c0b04-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c0b04-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c0b04-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c0b04-138">optional</span></span>  <br/> |<span data-ttu-id="c0b04-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="c0b04-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c0b04-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="c0b04-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c0b04-141">IX</span><span class="sxs-lookup"><span data-stu-id="c0b04-141">IX</span></span>  <br/> |<span data-ttu-id="c0b04-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c0b04-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c0b04-143">Optional</span><span class="sxs-lookup"><span data-stu-id="c0b04-143">optional</span></span>  <br/> |<span data-ttu-id="c0b04-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="c0b04-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c0b04-145">Es sollte eindeutigen und größer sein als andere Bezeichner im gleichen Abschnitt. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b04-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c0b04-146">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c0b04-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c0b04-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="c0b04-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c0b04-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c0b04-148">LocalName</span></span>  <br/> |<span data-ttu-id="c0b04-149">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0b04-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c0b04-150">Optional</span><span class="sxs-lookup"><span data-stu-id="c0b04-150">optional</span></span>  <br/> |<span data-ttu-id="c0b04-151">Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="c0b04-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c0b04-152">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c0b04-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c0b04-153">N</span><span class="sxs-lookup"><span data-stu-id="c0b04-153">N</span></span>  <br/> |<span data-ttu-id="c0b04-154">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0b04-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c0b04-155">Optional</span><span class="sxs-lookup"><span data-stu-id="c0b04-155">optional</span></span>  <br/> |<span data-ttu-id="c0b04-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b04-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c0b04-157">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c0b04-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c0b04-158">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c0b04-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c0b04-159">T</span><span class="sxs-lookup"><span data-stu-id="c0b04-159">T</span></span>  <br/> |<span data-ttu-id="c0b04-160">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c0b04-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c0b04-161">Optional</span><span class="sxs-lookup"><span data-stu-id="c0b04-161">optional</span></span>  <br/> |<span data-ttu-id="c0b04-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt wird und in der Geometrie Visualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0b04-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c0b04-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b04-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c0b04-164">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c0b04-164">Values of the xsd:string type.</span></span>  <br/> |
   

