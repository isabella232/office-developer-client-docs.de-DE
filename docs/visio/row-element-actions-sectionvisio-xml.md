---
title: Zeilenelement (Abschnitt "Actions") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356420"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="07779-103">Zeilenelement (Abschnitt "Actions") (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="07779-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="07779-104">Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07779-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07779-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="07779-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07779-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="07779-106">**Element type**</span></span> <br/> |[<span data-ttu-id="07779-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="07779-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="07779-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="07779-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="07779-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="07779-109">**Schema file**</span></span> <br/> |<span data-ttu-id="07779-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="07779-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="07779-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="07779-111">**Document parts**</span></span> <br/> |<span data-ttu-id="07779-112">"Masters. xml", "Master #. xml", "pages. xml", "page #. xml"</span><span class="sxs-lookup"><span data-stu-id="07779-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="07779-113">Definition</span><span class="sxs-lookup"><span data-stu-id="07779-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="07779-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="07779-114">Elements and attributes</span></span>

<span data-ttu-id="07779-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="07779-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="07779-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07779-116">Parent elements</span></span>

|<span data-ttu-id="07779-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="07779-117">**Element**</span></span>|<span data-ttu-id="07779-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="07779-118">**Type**</span></span>|<span data-ttu-id="07779-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07779-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="07779-120">Section</span><span class="sxs-lookup"><span data-stu-id="07779-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="07779-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="07779-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="07779-122">Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07779-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="07779-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07779-123">Child elements</span></span>

|<span data-ttu-id="07779-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="07779-124">**Element**</span></span>|<span data-ttu-id="07779-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="07779-125">**Type**</span></span>|<span data-ttu-id="07779-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07779-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="07779-127">Cell</span><span class="sxs-lookup"><span data-stu-id="07779-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="07779-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="07779-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="07779-129">Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07779-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="07779-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="07779-130">Attributes</span></span>

|<span data-ttu-id="07779-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="07779-131">**Attribute**</span></span>|<span data-ttu-id="07779-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="07779-132">**Type**</span></span>|<span data-ttu-id="07779-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="07779-133">**Required**</span></span>|<span data-ttu-id="07779-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07779-134">**Description**</span></span>|<span data-ttu-id="07779-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="07779-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="07779-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="07779-136">Del</span></span>  <br/> |<span data-ttu-id="07779-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="07779-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="07779-138">Optional</span><span class="sxs-lookup"><span data-stu-id="07779-138">optional</span></span>  <br/> |<span data-ttu-id="07779-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="07779-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="07779-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="07779-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="07779-141">IX</span><span class="sxs-lookup"><span data-stu-id="07779-141">IX</span></span>  <br/> |<span data-ttu-id="07779-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="07779-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="07779-143">Optional</span><span class="sxs-lookup"><span data-stu-id="07779-143">optional</span></span>  <br/> |<span data-ttu-id="07779-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="07779-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="07779-145">Sie sollte unqiue und größer sein als andere Bezeichner im gleichen Abschnitt. Das Attribut IX wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Rezensent, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="07779-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="07779-146">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="07779-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="07779-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="07779-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="07779-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="07779-148">LocalName</span></span>  <br/> |<span data-ttu-id="07779-149">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="07779-149">xsd:string</span></span>  <br/> |<span data-ttu-id="07779-150">Optional</span><span class="sxs-lookup"><span data-stu-id="07779-150">optional</span></span>  <br/> |<span data-ttu-id="07779-151">Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="07779-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="07779-152">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="07779-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="07779-153">N</span><span class="sxs-lookup"><span data-stu-id="07779-153">N</span></span>  <br/> |<span data-ttu-id="07779-154">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="07779-154">xsd:string</span></span>  <br/> |<span data-ttu-id="07779-155">Optional</span><span class="sxs-lookup"><span data-stu-id="07779-155">optional</span></span>  <br/> |<span data-ttu-id="07779-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="07779-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="07779-157">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="07779-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="07779-158">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="07779-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="07779-159">T</span><span class="sxs-lookup"><span data-stu-id="07779-159">T</span></span>  <br/> |<span data-ttu-id="07779-160">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="07779-160">xsd:string</span></span>  <br/> |<span data-ttu-id="07779-161">Optional</span><span class="sxs-lookup"><span data-stu-id="07779-161">optional</span></span>  <br/> |<span data-ttu-id="07779-162">Gibt den Typ des durch die Zeile dargestellten geometrischen Pfads an und wird in der Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="07779-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="07779-163">Das T-Attribut wird nur für den Abschnitt Geometry verwendet.</span><span class="sxs-lookup"><span data-stu-id="07779-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="07779-164">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="07779-164">Values of the xsd:string type.</span></span>  <br/> |
   

