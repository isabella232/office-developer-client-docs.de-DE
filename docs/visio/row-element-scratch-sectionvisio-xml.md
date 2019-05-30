---
title: Row-Element (Scratch section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541001"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="63135-103">Row-Element (Scratch section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="63135-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="63135-104">Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="63135-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63135-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="63135-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63135-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="63135-106">**Element type**</span></span> <br/> |[<span data-ttu-id="63135-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="63135-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="63135-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63135-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="63135-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="63135-109">**Schema file**</span></span> <br/> |<span data-ttu-id="63135-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="63135-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="63135-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="63135-111">**Document parts**</span></span> <br/> |<span data-ttu-id="63135-112">Document. XML, Masters. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="63135-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63135-113">Definition</span><span class="sxs-lookup"><span data-stu-id="63135-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="63135-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="63135-114">Elements and attributes</span></span>

<span data-ttu-id="63135-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="63135-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="63135-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63135-116">Parent elements</span></span>

|<span data-ttu-id="63135-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="63135-117">**Element**</span></span>|<span data-ttu-id="63135-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="63135-118">**Type**</span></span>|<span data-ttu-id="63135-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63135-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63135-120">Section</span><span class="sxs-lookup"><span data-stu-id="63135-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63135-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="63135-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63135-122">Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="63135-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="63135-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63135-123">Child elements</span></span>

|<span data-ttu-id="63135-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="63135-124">**Element**</span></span>|<span data-ttu-id="63135-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="63135-125">**Type**</span></span>|<span data-ttu-id="63135-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63135-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63135-127">Cell</span><span class="sxs-lookup"><span data-stu-id="63135-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="63135-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="63135-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63135-129">Gibt eine einzelne Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="63135-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="63135-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="63135-130">Attributes</span></span>

|<span data-ttu-id="63135-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="63135-131">**Attribute**</span></span>|<span data-ttu-id="63135-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="63135-132">**Type**</span></span>|<span data-ttu-id="63135-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="63135-133">**Required**</span></span>|<span data-ttu-id="63135-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63135-134">**Description**</span></span>|<span data-ttu-id="63135-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="63135-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="63135-136">Del</span><span class="sxs-lookup"><span data-stu-id="63135-136">Del</span></span>  <br/> |<span data-ttu-id="63135-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="63135-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="63135-138">Optional</span><span class="sxs-lookup"><span data-stu-id="63135-138">optional</span></span>  <br/> |<span data-ttu-id="63135-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="63135-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="63135-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="63135-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="63135-141">IX</span><span class="sxs-lookup"><span data-stu-id="63135-141">IX</span></span>  <br/> |<span data-ttu-id="63135-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63135-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63135-143">Optional</span><span class="sxs-lookup"><span data-stu-id="63135-143">optional</span></span>  <br/> |<span data-ttu-id="63135-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="63135-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="63135-145">Es sollte eindeutigen und größer sein als andere Bezeichner im gleichen Abschnitt. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="63135-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="63135-146">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63135-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="63135-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="63135-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="63135-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="63135-148">LocalName</span></span>  <br/> |<span data-ttu-id="63135-149">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="63135-149">xsd:string</span></span>  <br/> |<span data-ttu-id="63135-150">Optional</span><span class="sxs-lookup"><span data-stu-id="63135-150">optional</span></span>  <br/> |<span data-ttu-id="63135-151">Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="63135-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="63135-152">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="63135-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="63135-153">N</span><span class="sxs-lookup"><span data-stu-id="63135-153">N</span></span>  <br/> |<span data-ttu-id="63135-154">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="63135-154">xsd:string</span></span>  <br/> |<span data-ttu-id="63135-155">Optional</span><span class="sxs-lookup"><span data-stu-id="63135-155">optional</span></span>  <br/> |<span data-ttu-id="63135-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="63135-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="63135-157">Eine Zeile kann nur eines der Attribute IX oder N aufweisen.</span><span class="sxs-lookup"><span data-stu-id="63135-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="63135-158">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="63135-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="63135-159">T</span><span class="sxs-lookup"><span data-stu-id="63135-159">T</span></span>  <br/> |<span data-ttu-id="63135-160">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="63135-160">xsd:string</span></span>  <br/> |<span data-ttu-id="63135-161">Optional</span><span class="sxs-lookup"><span data-stu-id="63135-161">optional</span></span>  <br/> |<span data-ttu-id="63135-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt wird und in der Geometrie Visualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63135-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="63135-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="63135-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="63135-164">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="63135-164">Values of the xsd:string type.</span></span>  <br/> |
   

