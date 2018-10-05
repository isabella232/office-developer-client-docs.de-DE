---
title: Row-Element (Hyperlink Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: Enthält Elemente zum Erstellen mehrerer Liniensprünge zwischen einem Shape oder Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.
ms.openlocfilehash: 16935e463e76e0f0ee72b3fa40964551cf125cdd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400033"
---
# <a name="row-element-hyperlink-section-visio-xml"></a><span data-ttu-id="fd20c-103">Row-Element (Hyperlink Abschnitt) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="fd20c-103">Row element (Hyperlink Section) ('Visio XML')</span></span>

<span data-ttu-id="fd20c-104">Enthält Elemente zum Erstellen mehrerer Liniensprünge zwischen einem Shape oder Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.</span><span class="sxs-lookup"><span data-stu-id="fd20c-104">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd20c-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fd20c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd20c-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="fd20c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fd20c-107">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="fd20c-107">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fd20c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd20c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fd20c-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fd20c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fd20c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fd20c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fd20c-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="fd20c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fd20c-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="fd20c-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd20c-113">Definition</span><span class="sxs-lookup"><span data-stu-id="fd20c-113">Definition</span></span>

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fd20c-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fd20c-114">Elements and attributes</span></span>

<span data-ttu-id="fd20c-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="fd20c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fd20c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd20c-116">Parent elements</span></span>

|<span data-ttu-id="fd20c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd20c-117">**Element**</span></span>|<span data-ttu-id="fd20c-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fd20c-118">**Type**</span></span>|<span data-ttu-id="fd20c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd20c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd20c-120">Section</span><span class="sxs-lookup"><span data-stu-id="fd20c-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fd20c-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="fd20c-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fd20c-122">Enthält Elemente zum Erstellen mehrerer Liniensprünge zwischen einem Shape oder Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.</span><span class="sxs-lookup"><span data-stu-id="fd20c-122">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fd20c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd20c-123">Child elements</span></span>

|<span data-ttu-id="fd20c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd20c-124">**Element**</span></span>|<span data-ttu-id="fd20c-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fd20c-125">**Type**</span></span>|<span data-ttu-id="fd20c-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd20c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd20c-127">Cell</span><span class="sxs-lookup"><span data-stu-id="fd20c-127">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="fd20c-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fd20c-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fd20c-129">Enthält die Informationen für einen einzelnen Hyperlink, der mit einer Form verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="fd20c-129">Contains the information for a single hyperlink associated with a shape</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fd20c-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd20c-130">Attributes</span></span>

|<span data-ttu-id="fd20c-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fd20c-131">**Attribute**</span></span>|<span data-ttu-id="fd20c-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fd20c-132">**Type**</span></span>|<span data-ttu-id="fd20c-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="fd20c-133">**Required**</span></span>|<span data-ttu-id="fd20c-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd20c-134">**Description**</span></span>|<span data-ttu-id="fd20c-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="fd20c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd20c-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="fd20c-136">Del</span></span>  <br/> |<span data-ttu-id="fd20c-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="fd20c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fd20c-138">Optional</span><span class="sxs-lookup"><span data-stu-id="fd20c-138">optional</span></span>  <br/> |<span data-ttu-id="fd20c-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="fd20c-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="fd20c-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="fd20c-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fd20c-141">IX</span><span class="sxs-lookup"><span data-stu-id="fd20c-141">IX</span></span>  <br/> |<span data-ttu-id="fd20c-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fd20c-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fd20c-143">Optional</span><span class="sxs-lookup"><span data-stu-id="fd20c-143">optional</span></span>  <br/> |<span data-ttu-id="fd20c-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="fd20c-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="fd20c-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd20c-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="fd20c-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="fd20c-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="fd20c-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fd20c-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fd20c-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="fd20c-148">LocalName</span></span>  <br/> |<span data-ttu-id="fd20c-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fd20c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="fd20c-150">Optional</span><span class="sxs-lookup"><span data-stu-id="fd20c-150">optional</span></span>  <br/> |<span data-ttu-id="fd20c-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="fd20c-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="fd20c-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fd20c-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fd20c-153">N</span><span class="sxs-lookup"><span data-stu-id="fd20c-153">N</span></span>  <br/> |<span data-ttu-id="fd20c-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fd20c-154">xsd:string</span></span>  <br/> |<span data-ttu-id="fd20c-155">Optional</span><span class="sxs-lookup"><span data-stu-id="fd20c-155">optional</span></span>  <br/> |<span data-ttu-id="fd20c-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd20c-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="fd20c-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="fd20c-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="fd20c-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fd20c-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fd20c-159">T</span><span class="sxs-lookup"><span data-stu-id="fd20c-159">T</span></span>  <br/> |<span data-ttu-id="fd20c-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fd20c-160">xsd:string</span></span>  <br/> |<span data-ttu-id="fd20c-161">Optional</span><span class="sxs-lookup"><span data-stu-id="fd20c-161">optional</span></span>  <br/> |<span data-ttu-id="fd20c-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd20c-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="fd20c-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd20c-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="fd20c-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="fd20c-164">Values of the xsd:string type.</span></span>  <br/> |
   

