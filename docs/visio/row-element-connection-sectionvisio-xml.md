---
title: Row-Element (im Abschnitt Verbindung) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.
ms.openlocfilehash: 9f8f5f0735f7eeff2f1b2ec4562b79e6550d1716
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389918"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="fdee5-103">Row-Element (im Abschnitt Verbindung) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="fdee5-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="fdee5-104">Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.</span><span class="sxs-lookup"><span data-stu-id="fdee5-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fdee5-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fdee5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdee5-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="fdee5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fdee5-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="fdee5-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fdee5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fdee5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fdee5-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fdee5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fdee5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fdee5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fdee5-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="fdee5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fdee5-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="fdee5-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fdee5-113">Definition</span><span class="sxs-lookup"><span data-stu-id="fdee5-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fdee5-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fdee5-114">Elements and attributes</span></span>

<span data-ttu-id="fdee5-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="fdee5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fdee5-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fdee5-116">Parent elements</span></span>

|<span data-ttu-id="fdee5-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="fdee5-117">**Element**</span></span>|<span data-ttu-id="fdee5-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fdee5-118">**Type**</span></span>|<span data-ttu-id="fdee5-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fdee5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fdee5-120">Section</span><span class="sxs-lookup"><span data-stu-id="fdee5-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fdee5-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="fdee5-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fdee5-122">Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.</span><span class="sxs-lookup"><span data-stu-id="fdee5-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fdee5-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fdee5-123">Child elements</span></span>

|<span data-ttu-id="fdee5-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="fdee5-124">**Element**</span></span>|<span data-ttu-id="fdee5-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fdee5-125">**Type**</span></span>|<span data-ttu-id="fdee5-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fdee5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fdee5-127">Cell</span><span class="sxs-lookup"><span data-stu-id="fdee5-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="fdee5-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fdee5-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fdee5-129">Gibt eine einzelne Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="fdee5-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fdee5-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="fdee5-130">Attributes</span></span>

|<span data-ttu-id="fdee5-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fdee5-131">**Attribute**</span></span>|<span data-ttu-id="fdee5-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fdee5-132">**Type**</span></span>|<span data-ttu-id="fdee5-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="fdee5-133">**Required**</span></span>|<span data-ttu-id="fdee5-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fdee5-134">**Description**</span></span>|<span data-ttu-id="fdee5-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="fdee5-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fdee5-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="fdee5-136">Del</span></span>  <br/> |<span data-ttu-id="fdee5-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="fdee5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fdee5-138">Optional</span><span class="sxs-lookup"><span data-stu-id="fdee5-138">optional</span></span>  <br/> |<span data-ttu-id="fdee5-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="fdee5-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="fdee5-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="fdee5-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fdee5-141">IX</span><span class="sxs-lookup"><span data-stu-id="fdee5-141">IX</span></span>  <br/> |<span data-ttu-id="fdee5-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fdee5-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fdee5-143">Optional</span><span class="sxs-lookup"><span data-stu-id="fdee5-143">optional</span></span>  <br/> |<span data-ttu-id="fdee5-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="fdee5-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="fdee5-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdee5-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="fdee5-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="fdee5-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="fdee5-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fdee5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fdee5-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="fdee5-148">LocalName</span></span>  <br/> |<span data-ttu-id="fdee5-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fdee5-149">xsd:string</span></span>  <br/> |<span data-ttu-id="fdee5-150">Optional</span><span class="sxs-lookup"><span data-stu-id="fdee5-150">optional</span></span>  <br/> |<span data-ttu-id="fdee5-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="fdee5-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="fdee5-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fdee5-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fdee5-153">N</span><span class="sxs-lookup"><span data-stu-id="fdee5-153">N</span></span>  <br/> |<span data-ttu-id="fdee5-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fdee5-154">xsd:string</span></span>  <br/> |<span data-ttu-id="fdee5-155">Optional</span><span class="sxs-lookup"><span data-stu-id="fdee5-155">optional</span></span>  <br/> |<span data-ttu-id="fdee5-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdee5-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="fdee5-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="fdee5-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="fdee5-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fdee5-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fdee5-159">T</span><span class="sxs-lookup"><span data-stu-id="fdee5-159">T</span></span>  <br/> |<span data-ttu-id="fdee5-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fdee5-160">xsd:string</span></span>  <br/> |<span data-ttu-id="fdee5-161">Optional</span><span class="sxs-lookup"><span data-stu-id="fdee5-161">optional</span></span>  <br/> |<span data-ttu-id="fdee5-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdee5-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="fdee5-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdee5-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="fdee5-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fdee5-164">Values of the xsd:string type.</span></span>  <br/> |
   

