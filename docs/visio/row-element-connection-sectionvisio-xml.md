---
title: Row-Element (im Abschnitt Verbindung) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.
ms.openlocfilehash: d06a51e52f2b5273171d068f6fc2a6bf5227eed5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797897"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="8624b-103">Row-Element (im Abschnitt Verbindung) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="8624b-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="8624b-104">Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.</span><span class="sxs-lookup"><span data-stu-id="8624b-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8624b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8624b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8624b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="8624b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8624b-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="8624b-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8624b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8624b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8624b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="8624b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8624b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8624b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8624b-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="8624b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8624b-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="8624b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8624b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="8624b-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8624b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="8624b-114">Elements and attributes</span></span>

<span data-ttu-id="8624b-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8624b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8624b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8624b-116">Parent elements</span></span>

|<span data-ttu-id="8624b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8624b-117">**Element**</span></span>|<span data-ttu-id="8624b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8624b-118">**Type**</span></span>|<span data-ttu-id="8624b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8624b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8624b-120">Section</span><span class="sxs-lookup"><span data-stu-id="8624b-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8624b-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="8624b-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8624b-122">Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.</span><span class="sxs-lookup"><span data-stu-id="8624b-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8624b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8624b-123">Child elements</span></span>

|<span data-ttu-id="8624b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8624b-124">**Element**</span></span>|<span data-ttu-id="8624b-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8624b-125">**Type**</span></span>|<span data-ttu-id="8624b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8624b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8624b-127">Cell</span><span class="sxs-lookup"><span data-stu-id="8624b-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="8624b-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8624b-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8624b-129">Gibt eine einzelne Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="8624b-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8624b-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="8624b-130">Attributes</span></span>

|<span data-ttu-id="8624b-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8624b-131">**Attribute**</span></span>|<span data-ttu-id="8624b-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="8624b-132">**Type**</span></span>|<span data-ttu-id="8624b-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="8624b-133">**Required**</span></span>|<span data-ttu-id="8624b-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8624b-134">**Description**</span></span>|<span data-ttu-id="8624b-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="8624b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8624b-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="8624b-136">Del</span></span>  <br/> |<span data-ttu-id="8624b-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="8624b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8624b-138">Optional</span><span class="sxs-lookup"><span data-stu-id="8624b-138">optional</span></span>  <br/> |<span data-ttu-id="8624b-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="8624b-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="8624b-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8624b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8624b-141">IX</span><span class="sxs-lookup"><span data-stu-id="8624b-141">IX</span></span>  <br/> |<span data-ttu-id="8624b-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8624b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8624b-143">Optional</span><span class="sxs-lookup"><span data-stu-id="8624b-143">optional</span></span>  <br/> |<span data-ttu-id="8624b-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="8624b-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="8624b-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="8624b-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="8624b-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="8624b-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="8624b-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8624b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8624b-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="8624b-148">LocalName</span></span>  <br/> |<span data-ttu-id="8624b-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8624b-149">xsd:string</span></span>  <br/> |<span data-ttu-id="8624b-150">Optional</span><span class="sxs-lookup"><span data-stu-id="8624b-150">optional</span></span>  <br/> |<span data-ttu-id="8624b-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="8624b-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="8624b-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8624b-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8624b-153">N</span><span class="sxs-lookup"><span data-stu-id="8624b-153">N</span></span>  <br/> |<span data-ttu-id="8624b-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8624b-154">xsd:string</span></span>  <br/> |<span data-ttu-id="8624b-155">Optional</span><span class="sxs-lookup"><span data-stu-id="8624b-155">optional</span></span>  <br/> |<span data-ttu-id="8624b-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="8624b-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="8624b-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="8624b-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="8624b-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8624b-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8624b-159">T</span><span class="sxs-lookup"><span data-stu-id="8624b-159">T</span></span>  <br/> |<span data-ttu-id="8624b-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="8624b-160">xsd:string</span></span>  <br/> |<span data-ttu-id="8624b-161">Optional</span><span class="sxs-lookup"><span data-stu-id="8624b-161">optional</span></span>  <br/> |<span data-ttu-id="8624b-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8624b-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="8624b-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="8624b-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="8624b-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8624b-164">Values of the xsd:string type.</span></span>  <br/> |
   

