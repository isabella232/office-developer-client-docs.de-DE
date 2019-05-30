---
title: Row-Element (Aktions-Tag-Abschnitt) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Definiert ein Action-Tag auf einem Shape oder einer Seite.
ms.openlocfilehash: 44008d43871bfec9b5b943f19ce6ce0a069323d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540427"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="daef5-103">Row-Element (Aktions-Tag-Abschnitt) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="daef5-103">Row element (Action Tag Section) (Visio XML)</span></span>

<span data-ttu-id="daef5-104">Definiert ein Action-Tag auf einem Shape oder einer Seite.</span><span class="sxs-lookup"><span data-stu-id="daef5-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="daef5-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="daef5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="daef5-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="daef5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="daef5-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="daef5-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="daef5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="daef5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="daef5-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="daef5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="daef5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="daef5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="daef5-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="daef5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="daef5-112">Masters. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="daef5-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="daef5-113">Definition</span><span class="sxs-lookup"><span data-stu-id="daef5-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="daef5-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="daef5-114">Elements and attributes</span></span>

<span data-ttu-id="daef5-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="daef5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="daef5-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="daef5-116">Parent elements</span></span>

|<span data-ttu-id="daef5-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="daef5-117">**Element**</span></span>|<span data-ttu-id="daef5-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="daef5-118">**Type**</span></span>|<span data-ttu-id="daef5-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="daef5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="daef5-120">Section</span><span class="sxs-lookup"><span data-stu-id="daef5-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="daef5-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="daef5-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="daef5-122">Definiert ein Action-Tag auf einem Shape oder einer Seite.</span><span class="sxs-lookup"><span data-stu-id="daef5-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="daef5-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="daef5-123">Child elements</span></span>

|<span data-ttu-id="daef5-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="daef5-124">**Element**</span></span>|<span data-ttu-id="daef5-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="daef5-125">**Type**</span></span>|<span data-ttu-id="daef5-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="daef5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="daef5-127">Cell</span><span class="sxs-lookup"><span data-stu-id="daef5-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="daef5-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="daef5-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="daef5-129">Definiert eine Eigenschaft für ein Action-Tag auf einem Shape oder einer Seite.</span><span class="sxs-lookup"><span data-stu-id="daef5-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="daef5-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="daef5-130">Attributes</span></span>

|<span data-ttu-id="daef5-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="daef5-131">**Attribute**</span></span>|<span data-ttu-id="daef5-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="daef5-132">**Type**</span></span>|<span data-ttu-id="daef5-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="daef5-133">**Required**</span></span>|<span data-ttu-id="daef5-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="daef5-134">**Description**</span></span>|<span data-ttu-id="daef5-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="daef5-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="daef5-136">Del</span><span class="sxs-lookup"><span data-stu-id="daef5-136">Del</span></span>  <br/> |<span data-ttu-id="daef5-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="daef5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="daef5-138">Optional</span><span class="sxs-lookup"><span data-stu-id="daef5-138">optional</span></span>  <br/> |<span data-ttu-id="daef5-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="daef5-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="daef5-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="daef5-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="daef5-141">IX</span><span class="sxs-lookup"><span data-stu-id="daef5-141">IX</span></span>  <br/> |<span data-ttu-id="daef5-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="daef5-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="daef5-143">Optional</span><span class="sxs-lookup"><span data-stu-id="daef5-143">optional</span></span>  <br/> |<span data-ttu-id="daef5-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="daef5-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="daef5-145">Es sollte eindeutigen und größer sein als andere Bezeichner im gleichen Abschnitt. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="daef5-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="daef5-146">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="daef5-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="daef5-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="daef5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="daef5-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="daef5-148">LocalName</span></span>  <br/> |<span data-ttu-id="daef5-149">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="daef5-149">xsd:string</span></span>  <br/> |<span data-ttu-id="daef5-150">Optional</span><span class="sxs-lookup"><span data-stu-id="daef5-150">optional</span></span>  <br/> |<span data-ttu-id="daef5-151">Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="daef5-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="daef5-152">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="daef5-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="daef5-153">N</span><span class="sxs-lookup"><span data-stu-id="daef5-153">N</span></span>  <br/> |<span data-ttu-id="daef5-154">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="daef5-154">xsd:string</span></span>  <br/> |<span data-ttu-id="daef5-155">Optional</span><span class="sxs-lookup"><span data-stu-id="daef5-155">optional</span></span>  <br/> |<span data-ttu-id="daef5-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="daef5-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="daef5-157">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="daef5-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="daef5-158">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="daef5-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="daef5-159">T</span><span class="sxs-lookup"><span data-stu-id="daef5-159">T</span></span>  <br/> |<span data-ttu-id="daef5-160">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="daef5-160">xsd:string</span></span>  <br/> |<span data-ttu-id="daef5-161">Optional</span><span class="sxs-lookup"><span data-stu-id="daef5-161">optional</span></span>  <br/> |<span data-ttu-id="daef5-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt wird und in der Geometrie Visualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="daef5-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="daef5-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="daef5-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="daef5-164">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="daef5-164">Values of the xsd:string type.</span></span>  <br/> |
   

