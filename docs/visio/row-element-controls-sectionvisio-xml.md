---
title: Row-Element (Abschnitt "Controls") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Enthält Zellen für ein bestimmtes Steuerpunkt eines Shapes definiert.
ms.openlocfilehash: aa690bf70078a711dffca3f01b6e7acc05507bdd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386768"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="d0130-103">Row-Element (Abschnitt "Controls") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d0130-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="d0130-104">Enthält Zellen für ein bestimmtes Steuerpunkt eines Shapes definiert.</span><span class="sxs-lookup"><span data-stu-id="d0130-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0130-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d0130-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0130-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d0130-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d0130-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="d0130-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d0130-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0130-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d0130-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d0130-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d0130-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d0130-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d0130-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="d0130-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d0130-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="d0130-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0130-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d0130-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0130-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d0130-114">Elements and attributes</span></span>

<span data-ttu-id="d0130-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d0130-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d0130-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0130-116">Parent elements</span></span>

|<span data-ttu-id="d0130-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0130-117">**Element**</span></span>|<span data-ttu-id="d0130-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d0130-118">**Type**</span></span>|<span data-ttu-id="d0130-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0130-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0130-120">Section</span><span class="sxs-lookup"><span data-stu-id="d0130-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0130-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d0130-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0130-122">Enthält Zellen für ein bestimmtes Steuerpunkt eines Shapes definiert.</span><span class="sxs-lookup"><span data-stu-id="d0130-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d0130-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0130-123">Child elements</span></span>

|<span data-ttu-id="d0130-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0130-124">**Element**</span></span>|<span data-ttu-id="d0130-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d0130-125">**Type**</span></span>|<span data-ttu-id="d0130-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0130-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0130-127">Cell</span><span class="sxs-lookup"><span data-stu-id="d0130-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="d0130-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d0130-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0130-129">Enthält eine Eigenschaft für ein bestimmtes Steuerpunkt eines Shapes definiert.</span><span class="sxs-lookup"><span data-stu-id="d0130-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d0130-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0130-130">Attributes</span></span>

|<span data-ttu-id="d0130-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d0130-131">**Attribute**</span></span>|<span data-ttu-id="d0130-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d0130-132">**Type**</span></span>|<span data-ttu-id="d0130-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d0130-133">**Required**</span></span>|<span data-ttu-id="d0130-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0130-134">**Description**</span></span>|<span data-ttu-id="d0130-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d0130-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0130-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="d0130-136">Del</span></span>  <br/> |<span data-ttu-id="d0130-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="d0130-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d0130-138">Optional</span><span class="sxs-lookup"><span data-stu-id="d0130-138">optional</span></span>  <br/> |<span data-ttu-id="d0130-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d0130-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="d0130-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="d0130-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d0130-141">IX</span><span class="sxs-lookup"><span data-stu-id="d0130-141">IX</span></span>  <br/> |<span data-ttu-id="d0130-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0130-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0130-143">Optional</span><span class="sxs-lookup"><span data-stu-id="d0130-143">optional</span></span>  <br/> |<span data-ttu-id="d0130-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="d0130-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="d0130-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0130-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="d0130-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="d0130-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d0130-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d0130-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d0130-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="d0130-148">LocalName</span></span>  <br/> |<span data-ttu-id="d0130-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d0130-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d0130-150">Optional</span><span class="sxs-lookup"><span data-stu-id="d0130-150">optional</span></span>  <br/> |<span data-ttu-id="d0130-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="d0130-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="d0130-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d0130-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0130-153">N</span><span class="sxs-lookup"><span data-stu-id="d0130-153">N</span></span>  <br/> |<span data-ttu-id="d0130-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d0130-154">xsd:string</span></span>  <br/> |<span data-ttu-id="d0130-155">Optional</span><span class="sxs-lookup"><span data-stu-id="d0130-155">optional</span></span>  <br/> |<span data-ttu-id="d0130-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0130-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="d0130-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="d0130-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d0130-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d0130-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0130-159">T</span><span class="sxs-lookup"><span data-stu-id="d0130-159">T</span></span>  <br/> |<span data-ttu-id="d0130-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="d0130-160">xsd:string</span></span>  <br/> |<span data-ttu-id="d0130-161">Optional</span><span class="sxs-lookup"><span data-stu-id="d0130-161">optional</span></span>  <br/> |<span data-ttu-id="d0130-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0130-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="d0130-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0130-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="d0130-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d0130-164">Values of the xsd:string type.</span></span>  <br/> |
   

