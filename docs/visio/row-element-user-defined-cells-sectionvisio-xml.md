---
title: Row-Element (User-defined Cells Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Eine vom Benutzer angegebener Informationseinheit, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.
ms.openlocfilehash: 8852c1db31e9a9b8f0860c111da32de6d44dc7f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388014"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="9b122-103">Row-Element (User-defined Cells Abschnitt) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="9b122-103">Row element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="9b122-104">Eine vom Benutzer angegebener Informationseinheit, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b122-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b122-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9b122-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b122-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9b122-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9b122-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="9b122-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9b122-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9b122-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9b122-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9b122-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9b122-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9b122-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9b122-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="9b122-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9b122-112">Document.XML, masters.xml, Master-Shape # .xml, pages.xml, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="9b122-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9b122-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9b122-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9b122-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9b122-114">Elements and attributes</span></span>

<span data-ttu-id="9b122-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="9b122-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9b122-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b122-116">Parent elements</span></span>

|<span data-ttu-id="9b122-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b122-117">**Element**</span></span>|<span data-ttu-id="9b122-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9b122-118">**Type**</span></span>|<span data-ttu-id="9b122-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b122-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b122-120">Section</span><span class="sxs-lookup"><span data-stu-id="9b122-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9b122-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9b122-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9b122-122">Eine vom Benutzer angegebener Informationseinheit, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b122-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b122-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b122-123">Child elements</span></span>

|<span data-ttu-id="9b122-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b122-124">**Element**</span></span>|<span data-ttu-id="9b122-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9b122-125">**Type**</span></span>|<span data-ttu-id="9b122-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b122-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9b122-127">Cell</span><span class="sxs-lookup"><span data-stu-id="9b122-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9b122-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9b122-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9b122-129">Eine Eigenschaft eines vom Benutzer angegebener bestimmte Informationen, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b122-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9b122-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b122-130">Attributes</span></span>

|<span data-ttu-id="9b122-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9b122-131">**Attribute**</span></span>|<span data-ttu-id="9b122-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9b122-132">**Type**</span></span>|<span data-ttu-id="9b122-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9b122-133">**Required**</span></span>|<span data-ttu-id="9b122-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b122-134">**Description**</span></span>|<span data-ttu-id="9b122-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9b122-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9b122-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="9b122-136">Del</span></span>  <br/> |<span data-ttu-id="9b122-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="9b122-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9b122-138">Optional</span><span class="sxs-lookup"><span data-stu-id="9b122-138">optional</span></span>  <br/> |<span data-ttu-id="9b122-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="9b122-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="9b122-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="9b122-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9b122-141">IX</span><span class="sxs-lookup"><span data-stu-id="9b122-141">IX</span></span>  <br/> |<span data-ttu-id="9b122-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9b122-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9b122-143">Optional</span><span class="sxs-lookup"><span data-stu-id="9b122-143">optional</span></span>  <br/> |<span data-ttu-id="9b122-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="9b122-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="9b122-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b122-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="9b122-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="9b122-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9b122-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9b122-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9b122-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="9b122-148">LocalName</span></span>  <br/> |<span data-ttu-id="9b122-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9b122-149">xsd:string</span></span>  <br/> |<span data-ttu-id="9b122-150">Optional</span><span class="sxs-lookup"><span data-stu-id="9b122-150">optional</span></span>  <br/> |<span data-ttu-id="9b122-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="9b122-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="9b122-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9b122-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9b122-153">N</span><span class="sxs-lookup"><span data-stu-id="9b122-153">N</span></span>  <br/> |<span data-ttu-id="9b122-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9b122-154">xsd:string</span></span>  <br/> |<span data-ttu-id="9b122-155">Optional</span><span class="sxs-lookup"><span data-stu-id="9b122-155">optional</span></span>  <br/> |<span data-ttu-id="9b122-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b122-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="9b122-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="9b122-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="9b122-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9b122-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9b122-159">T</span><span class="sxs-lookup"><span data-stu-id="9b122-159">T</span></span>  <br/> |<span data-ttu-id="9b122-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9b122-160">xsd:string</span></span>  <br/> |<span data-ttu-id="9b122-161">Optional</span><span class="sxs-lookup"><span data-stu-id="9b122-161">optional</span></span>  <br/> |<span data-ttu-id="9b122-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b122-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="9b122-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b122-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="9b122-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9b122-164">Values of the xsd:string type.</span></span>  <br/> |
   

