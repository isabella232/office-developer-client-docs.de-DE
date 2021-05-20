---
title: Row-Element (Abschnitt "User-defined Cells") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Eine vom Benutzer angegebene Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538172"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="1e419-103">Row-Element (Abschnitt "User-defined Cells") (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1e419-103">Row element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="1e419-104">Eine vom Benutzer angegebene Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e419-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e419-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1e419-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e419-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1e419-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1e419-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="1e419-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1e419-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e419-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1e419-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1e419-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1e419-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1e419-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1e419-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="1e419-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1e419-112">document.xml, masters.xml, Master#.xml, pages.xml, Seite#.xml</span><span class="sxs-lookup"><span data-stu-id="1e419-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e419-113">Definition</span><span class="sxs-lookup"><span data-stu-id="1e419-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1e419-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1e419-114">Elements and attributes</span></span>

<span data-ttu-id="1e419-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1e419-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1e419-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e419-116">Parent elements</span></span>

|<span data-ttu-id="1e419-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e419-117">**Element**</span></span>|<span data-ttu-id="1e419-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1e419-118">**Type**</span></span>|<span data-ttu-id="1e419-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e419-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e419-120">Section</span><span class="sxs-lookup"><span data-stu-id="1e419-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1e419-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1e419-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1e419-122">Eine vom Benutzer angegebene Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e419-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1e419-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e419-123">Child elements</span></span>

|<span data-ttu-id="1e419-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e419-124">**Element**</span></span>|<span data-ttu-id="1e419-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1e419-125">**Type**</span></span>|<span data-ttu-id="1e419-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e419-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e419-127">Cell</span><span class="sxs-lookup"><span data-stu-id="1e419-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1e419-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1e419-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1e419-129">Eine Eigenschaft eines benutzerdefinierten Informationsteils, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e419-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1e419-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e419-130">Attributes</span></span>

|<span data-ttu-id="1e419-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1e419-131">**Attribute**</span></span>|<span data-ttu-id="1e419-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1e419-132">**Type**</span></span>|<span data-ttu-id="1e419-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1e419-133">**Required**</span></span>|<span data-ttu-id="1e419-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e419-134">**Description**</span></span>|<span data-ttu-id="1e419-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1e419-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e419-136">Del</span><span class="sxs-lookup"><span data-stu-id="1e419-136">Del</span></span>  <br/> |<span data-ttu-id="1e419-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1e419-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1e419-138">Optional</span><span class="sxs-lookup"><span data-stu-id="1e419-138">optional</span></span>  <br/> |<span data-ttu-id="1e419-139">Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="1e419-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="1e419-140">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1e419-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1e419-141">IX</span><span class="sxs-lookup"><span data-stu-id="1e419-141">IX</span></span>  <br/> |<span data-ttu-id="1e419-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1e419-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1e419-143">Optional</span><span class="sxs-lookup"><span data-stu-id="1e419-143">optional</span></span>  <br/> |<span data-ttu-id="1e419-144">Gibt den 1-basierten Bezeichner für die Zeile an.</span><span class="sxs-lookup"><span data-stu-id="1e419-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="1e419-145">Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e419-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="1e419-146">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1e419-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1e419-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="1e419-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1e419-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="1e419-148">LocalName</span></span>  <br/> |<span data-ttu-id="1e419-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e419-149">xsd:string</span></span>  <br/> |<span data-ttu-id="1e419-150">Optional</span><span class="sxs-lookup"><span data-stu-id="1e419-150">optional</span></span>  <br/> |<span data-ttu-id="1e419-151">Gibt den eindeutigen sprachabhängigen Namen der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="1e419-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="1e419-152">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1e419-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e419-153">N</span><span class="sxs-lookup"><span data-stu-id="1e419-153">N</span></span>  <br/> |<span data-ttu-id="1e419-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e419-154">xsd:string</span></span>  <br/> |<span data-ttu-id="1e419-155">Optional</span><span class="sxs-lookup"><span data-stu-id="1e419-155">optional</span></span>  <br/> |<span data-ttu-id="1e419-156">Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e419-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="1e419-157">Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1e419-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1e419-158">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1e419-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e419-159">T</span><span class="sxs-lookup"><span data-stu-id="1e419-159">T</span></span>  <br/> |<span data-ttu-id="1e419-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e419-160">xsd:string</span></span>  <br/> |<span data-ttu-id="1e419-161">Optional</span><span class="sxs-lookup"><span data-stu-id="1e419-161">optional</span></span>  <br/> |<span data-ttu-id="1e419-162">Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e419-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="1e419-163">Das T-Attribut wird nur für den Abschnitt Geometry verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e419-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="1e419-164">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="1e419-164">Values of the xsd:string type.</span></span>  <br/> |
   

