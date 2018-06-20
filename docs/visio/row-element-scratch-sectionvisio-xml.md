---
title: Row-Element (Abschnitt "Scratch") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.
ms.openlocfilehash: 078205b08ab40c2b88320779b1fbabc31c781eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797915"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="25468-103">Row-Element (Abschnitt "Scratch") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="25468-103">Row element (Scratch Section) ('Visio XML')</span></span>

<span data-ttu-id="25468-104">Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="25468-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25468-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="25468-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25468-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="25468-106">**Element type**</span></span> <br/> |[<span data-ttu-id="25468-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="25468-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="25468-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="25468-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="25468-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="25468-109">**Schema file**</span></span> <br/> |<span data-ttu-id="25468-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="25468-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="25468-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="25468-111">**Document parts**</span></span> <br/> |<span data-ttu-id="25468-112">Document.XML, masters.xml, Master-Shape # .xml, pages.xml, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="25468-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="25468-113">Definition</span><span class="sxs-lookup"><span data-stu-id="25468-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="25468-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="25468-114">Elements and attributes</span></span>

<span data-ttu-id="25468-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="25468-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="25468-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25468-116">Parent elements</span></span>

|<span data-ttu-id="25468-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="25468-117">**Element**</span></span>|<span data-ttu-id="25468-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="25468-118">**Type**</span></span>|<span data-ttu-id="25468-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25468-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="25468-120">Section</span><span class="sxs-lookup"><span data-stu-id="25468-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="25468-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="25468-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="25468-122">Eine Arbeitsumgebung für die Eingabe und das Testen von Formeln, auf die von anderen Zellen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="25468-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="25468-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25468-123">Child elements</span></span>

|<span data-ttu-id="25468-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="25468-124">**Element**</span></span>|<span data-ttu-id="25468-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="25468-125">**Type**</span></span>|<span data-ttu-id="25468-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25468-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="25468-127">Cell</span><span class="sxs-lookup"><span data-stu-id="25468-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="25468-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="25468-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="25468-129">Gibt eine einzelne Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="25468-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="25468-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="25468-130">Attributes</span></span>

|<span data-ttu-id="25468-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="25468-131">**Attribute**</span></span>|<span data-ttu-id="25468-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="25468-132">**Type**</span></span>|<span data-ttu-id="25468-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="25468-133">**Required**</span></span>|<span data-ttu-id="25468-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25468-134">**Description**</span></span>|<span data-ttu-id="25468-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="25468-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="25468-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="25468-136">Del</span></span>  <br/> |<span data-ttu-id="25468-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="25468-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="25468-138">Optional</span><span class="sxs-lookup"><span data-stu-id="25468-138">optional</span></span>  <br/> |<span data-ttu-id="25468-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="25468-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="25468-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="25468-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="25468-141">IX</span><span class="sxs-lookup"><span data-stu-id="25468-141">IX</span></span>  <br/> |<span data-ttu-id="25468-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="25468-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="25468-143">Optional</span><span class="sxs-lookup"><span data-stu-id="25468-143">optional</span></span>  <br/> |<span data-ttu-id="25468-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="25468-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="25468-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="25468-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="25468-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="25468-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="25468-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="25468-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="25468-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="25468-148">LocalName</span></span>  <br/> |<span data-ttu-id="25468-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="25468-149">xsd:string</span></span>  <br/> |<span data-ttu-id="25468-150">Optional</span><span class="sxs-lookup"><span data-stu-id="25468-150">optional</span></span>  <br/> |<span data-ttu-id="25468-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="25468-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="25468-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="25468-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="25468-153">N</span><span class="sxs-lookup"><span data-stu-id="25468-153">N</span></span>  <br/> |<span data-ttu-id="25468-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="25468-154">xsd:string</span></span>  <br/> |<span data-ttu-id="25468-155">Optional</span><span class="sxs-lookup"><span data-stu-id="25468-155">optional</span></span>  <br/> |<span data-ttu-id="25468-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="25468-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="25468-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="25468-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="25468-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="25468-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="25468-159">T</span><span class="sxs-lookup"><span data-stu-id="25468-159">T</span></span>  <br/> |<span data-ttu-id="25468-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="25468-160">xsd:string</span></span>  <br/> |<span data-ttu-id="25468-161">Optional</span><span class="sxs-lookup"><span data-stu-id="25468-161">optional</span></span>  <br/> |<span data-ttu-id="25468-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="25468-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="25468-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="25468-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="25468-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="25468-164">Values of the xsd:string type.</span></span>  <br/> |
   

