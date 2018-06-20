---
title: Row-Element (Feldabschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Zeigt Funktionen und Formeln, die über das Dialogfeld Feld in den Text des Shapes eingefügt.
ms.openlocfilehash: ec01ae3743eaf5345685c7273404bfdb826579ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797918"
---
# <a name="row-element-field-section-visio-xml"></a><span data-ttu-id="68efe-103">Row-Element (Feldabschnitt) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="68efe-103">Row element (Field Section) ('Visio XML')</span></span>

<span data-ttu-id="68efe-104">Zeigt Funktionen und Formeln, die über das Dialogfeld Feld in den Text des Shapes eingefügt.</span><span class="sxs-lookup"><span data-stu-id="68efe-104">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68efe-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68efe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68efe-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="68efe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68efe-107">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="68efe-107">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68efe-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68efe-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68efe-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="68efe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68efe-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="68efe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68efe-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="68efe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68efe-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="68efe-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68efe-113">Definition</span><span class="sxs-lookup"><span data-stu-id="68efe-113">Definition</span></span>

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68efe-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="68efe-114">Elements and attributes</span></span>

<span data-ttu-id="68efe-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="68efe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68efe-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68efe-116">Parent elements</span></span>

|<span data-ttu-id="68efe-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="68efe-117">**Element**</span></span>|<span data-ttu-id="68efe-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68efe-118">**Type**</span></span>|<span data-ttu-id="68efe-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68efe-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68efe-120">Section</span><span class="sxs-lookup"><span data-stu-id="68efe-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68efe-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="68efe-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68efe-122">Zeigt Funktionen und Formeln, die über das Dialogfeld Feld in den Text des Shapes eingefügt.</span><span class="sxs-lookup"><span data-stu-id="68efe-122">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68efe-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68efe-123">Child elements</span></span>

|<span data-ttu-id="68efe-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="68efe-124">**Element**</span></span>|<span data-ttu-id="68efe-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68efe-125">**Type**</span></span>|<span data-ttu-id="68efe-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68efe-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68efe-127">Cell</span><span class="sxs-lookup"><span data-stu-id="68efe-127">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="68efe-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="68efe-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68efe-129">Zeigt Funktionen und Formeln, die über das Dialogfeld Feld in den Text des Shapes eingefügt</span><span class="sxs-lookup"><span data-stu-id="68efe-129">Displays functions and formulas inserted in the shape's text by using the Field dialog box</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68efe-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="68efe-130">Attributes</span></span>

|<span data-ttu-id="68efe-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68efe-131">**Attribute**</span></span>|<span data-ttu-id="68efe-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68efe-132">**Type**</span></span>|<span data-ttu-id="68efe-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="68efe-133">**Required**</span></span>|<span data-ttu-id="68efe-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68efe-134">**Description**</span></span>|<span data-ttu-id="68efe-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="68efe-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68efe-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="68efe-136">Del</span></span>  <br/> |<span data-ttu-id="68efe-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="68efe-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="68efe-138">Optional</span><span class="sxs-lookup"><span data-stu-id="68efe-138">optional</span></span>  <br/> |<span data-ttu-id="68efe-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="68efe-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="68efe-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="68efe-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="68efe-141">IX</span><span class="sxs-lookup"><span data-stu-id="68efe-141">IX</span></span>  <br/> |<span data-ttu-id="68efe-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68efe-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68efe-143">Optional</span><span class="sxs-lookup"><span data-stu-id="68efe-143">optional</span></span>  <br/> |<span data-ttu-id="68efe-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="68efe-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="68efe-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="68efe-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="68efe-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="68efe-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="68efe-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="68efe-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68efe-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="68efe-148">LocalName</span></span>  <br/> |<span data-ttu-id="68efe-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="68efe-149">xsd:string</span></span>  <br/> |<span data-ttu-id="68efe-150">Optional</span><span class="sxs-lookup"><span data-stu-id="68efe-150">optional</span></span>  <br/> |<span data-ttu-id="68efe-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="68efe-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="68efe-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="68efe-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="68efe-153">N</span><span class="sxs-lookup"><span data-stu-id="68efe-153">N</span></span>  <br/> |<span data-ttu-id="68efe-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="68efe-154">xsd:string</span></span>  <br/> |<span data-ttu-id="68efe-155">Optional</span><span class="sxs-lookup"><span data-stu-id="68efe-155">optional</span></span>  <br/> |<span data-ttu-id="68efe-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="68efe-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="68efe-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="68efe-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="68efe-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="68efe-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="68efe-159">T</span><span class="sxs-lookup"><span data-stu-id="68efe-159">T</span></span>  <br/> |<span data-ttu-id="68efe-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="68efe-160">xsd:string</span></span>  <br/> |<span data-ttu-id="68efe-161">Optional</span><span class="sxs-lookup"><span data-stu-id="68efe-161">optional</span></span>  <br/> |<span data-ttu-id="68efe-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="68efe-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="68efe-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="68efe-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="68efe-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="68efe-164">Values of the xsd:string type.</span></span>  <br/> |
   

