---
title: Row-Element (Abschnitt "Actions") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.
ms.openlocfilehash: 67ddbf633a93a8295667d10d8957828ff4c76bfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797887"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="ccbd4-103">Row-Element (Abschnitt "Actions") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ccbd4-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="ccbd4-104">Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccbd4-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ccbd4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccbd4-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ccbd4-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="ccbd4-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ccbd4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ccbd4-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ccbd4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ccbd4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ccbd4-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ccbd4-112">Masters.XML, Master-Shape # .xml, pages.xml, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="ccbd4-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ccbd4-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ccbd4-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ccbd4-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ccbd4-114">Elements and attributes</span></span>

<span data-ttu-id="ccbd4-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ccbd4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ccbd4-116">Parent elements</span></span>

|<span data-ttu-id="ccbd4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-117">**Element**</span></span>|<span data-ttu-id="ccbd4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-118">**Type**</span></span>|<span data-ttu-id="ccbd4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ccbd4-120">Section</span><span class="sxs-lookup"><span data-stu-id="ccbd4-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ccbd4-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ccbd4-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccbd4-122">Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ccbd4-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ccbd4-123">Child elements</span></span>

|<span data-ttu-id="ccbd4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-124">**Element**</span></span>|<span data-ttu-id="ccbd4-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-125">**Type**</span></span>|<span data-ttu-id="ccbd4-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ccbd4-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ccbd4-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="ccbd4-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ccbd4-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccbd4-129">Gibt eine Eigenschaft einer Aktion in einem Kontext- oder Aktionstagmenü eines benutzerdefinierten Befehls zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ccbd4-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="ccbd4-130">Attributes</span></span>

|<span data-ttu-id="ccbd4-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-131">**Attribute**</span></span>|<span data-ttu-id="ccbd4-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-132">**Type**</span></span>|<span data-ttu-id="ccbd4-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-133">**Required**</span></span>|<span data-ttu-id="ccbd4-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-134">**Description**</span></span>|<span data-ttu-id="ccbd4-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ccbd4-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ccbd4-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="ccbd4-136">Del</span></span>  <br/> |<span data-ttu-id="ccbd4-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ccbd4-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ccbd4-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ccbd4-138">optional</span></span>  <br/> |<span data-ttu-id="ccbd4-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="ccbd4-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ccbd4-141">IX</span><span class="sxs-lookup"><span data-stu-id="ccbd4-141">IX</span></span>  <br/> |<span data-ttu-id="ccbd4-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ccbd4-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ccbd4-143">Optional</span><span class="sxs-lookup"><span data-stu-id="ccbd4-143">optional</span></span>  <br/> |<span data-ttu-id="ccbd4-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="ccbd4-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="ccbd4-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ccbd4-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ccbd4-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="ccbd4-148">LocalName</span></span>  <br/> |<span data-ttu-id="ccbd4-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ccbd4-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ccbd4-150">Optional</span><span class="sxs-lookup"><span data-stu-id="ccbd4-150">optional</span></span>  <br/> |<span data-ttu-id="ccbd4-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="ccbd4-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ccbd4-153">N</span><span class="sxs-lookup"><span data-stu-id="ccbd4-153">N</span></span>  <br/> |<span data-ttu-id="ccbd4-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ccbd4-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ccbd4-155">Optional</span><span class="sxs-lookup"><span data-stu-id="ccbd4-155">optional</span></span>  <br/> |<span data-ttu-id="ccbd4-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="ccbd4-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ccbd4-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ccbd4-159">T</span><span class="sxs-lookup"><span data-stu-id="ccbd4-159">T</span></span>  <br/> |<span data-ttu-id="ccbd4-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ccbd4-160">xsd:string</span></span>  <br/> |<span data-ttu-id="ccbd4-161">Optional</span><span class="sxs-lookup"><span data-stu-id="ccbd4-161">optional</span></span>  <br/> |<span data-ttu-id="ccbd4-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="ccbd4-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="ccbd4-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ccbd4-164">Values of the xsd:string type.</span></span>  <br/> |
   

