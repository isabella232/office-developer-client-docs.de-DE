---
title: Row-Element (Abschnitt "Shape Data") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Gibt ein Shape-Dateneingabe zum Zuordnen von Daten mit einer Form an.
ms.openlocfilehash: 7857ad8a28e11d6ed3ba34145ffc0606f306120f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385508"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="1c232-103">Row-Element (Abschnitt "Shape Data") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="1c232-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="1c232-104">Gibt ein Shape-Dateneingabe zum Zuordnen von Daten mit einer Form an.</span><span class="sxs-lookup"><span data-stu-id="1c232-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c232-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1c232-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c232-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1c232-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1c232-107">Shape-Datentyp</span><span class="sxs-lookup"><span data-stu-id="1c232-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1c232-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1c232-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1c232-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1c232-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1c232-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1c232-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1c232-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="1c232-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1c232-112"># .xml Master, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="1c232-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c232-113">Definition</span><span class="sxs-lookup"><span data-stu-id="1c232-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1c232-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1c232-114">Elements and attributes</span></span>

<span data-ttu-id="1c232-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="1c232-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1c232-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c232-116">Parent elements</span></span>

|<span data-ttu-id="1c232-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c232-117">**Element**</span></span>|<span data-ttu-id="1c232-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1c232-118">**Type**</span></span>|<span data-ttu-id="1c232-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c232-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c232-120">Section</span><span class="sxs-lookup"><span data-stu-id="1c232-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c232-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1c232-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c232-122">Gibt ein Shape-Dateneingabe zum Zuordnen von Daten mit einer Form an.</span><span class="sxs-lookup"><span data-stu-id="1c232-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1c232-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c232-123">Child elements</span></span>

|<span data-ttu-id="1c232-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c232-124">**Element**</span></span>|<span data-ttu-id="1c232-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1c232-125">**Type**</span></span>|<span data-ttu-id="1c232-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c232-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c232-127">Cell</span><span class="sxs-lookup"><span data-stu-id="1c232-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1c232-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1c232-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c232-129">Gibt eine Eigenschaft eines Shape-Daten an.</span><span class="sxs-lookup"><span data-stu-id="1c232-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1c232-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c232-130">Attributes</span></span>

|<span data-ttu-id="1c232-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1c232-131">**Attribute**</span></span>|<span data-ttu-id="1c232-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1c232-132">**Type**</span></span>|<span data-ttu-id="1c232-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1c232-133">**Required**</span></span>|<span data-ttu-id="1c232-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c232-134">**Description**</span></span>|<span data-ttu-id="1c232-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1c232-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c232-136">ENTF</span><span class="sxs-lookup"><span data-stu-id="1c232-136">Del</span></span>  <br/> |<span data-ttu-id="1c232-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="1c232-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1c232-138">Optional</span><span class="sxs-lookup"><span data-stu-id="1c232-138">optional</span></span>  <br/> |<span data-ttu-id="1c232-139">Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="1c232-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="1c232-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c232-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1c232-141">IX</span><span class="sxs-lookup"><span data-stu-id="1c232-141">IX</span></span>  <br/> |<span data-ttu-id="1c232-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1c232-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1c232-143">Optional</span><span class="sxs-lookup"><span data-stu-id="1c232-143">optional</span></span>  <br/> |<span data-ttu-id="1c232-144">Gibt den Bezeichner eins für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="1c232-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="1c232-145">Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c232-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="1c232-146">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="1c232-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1c232-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1c232-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1c232-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="1c232-148">LocalName</span></span>  <br/> |<span data-ttu-id="1c232-149">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1c232-149">xsd:string</span></span>  <br/> |<span data-ttu-id="1c232-150">Optional</span><span class="sxs-lookup"><span data-stu-id="1c232-150">optional</span></span>  <br/> |<span data-ttu-id="1c232-151">Gibt den eindeutigen Namen der Sprache ab der Zeile an.</span><span class="sxs-lookup"><span data-stu-id="1c232-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="1c232-152">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1c232-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c232-153">N</span><span class="sxs-lookup"><span data-stu-id="1c232-153">N</span></span>  <br/> |<span data-ttu-id="1c232-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1c232-154">xsd:string</span></span>  <br/> |<span data-ttu-id="1c232-155">Optional</span><span class="sxs-lookup"><span data-stu-id="1c232-155">optional</span></span>  <br/> |<span data-ttu-id="1c232-156">Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c232-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="1c232-157">Eine Zeile können Sie nur die Attribute IX oder N haben.</span><span class="sxs-lookup"><span data-stu-id="1c232-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="1c232-158">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1c232-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c232-159">T</span><span class="sxs-lookup"><span data-stu-id="1c232-159">T</span></span>  <br/> |<span data-ttu-id="1c232-160">XSD: String</span><span class="sxs-lookup"><span data-stu-id="1c232-160">xsd:string</span></span>  <br/> |<span data-ttu-id="1c232-161">Optional</span><span class="sxs-lookup"><span data-stu-id="1c232-161">optional</span></span>  <br/> |<span data-ttu-id="1c232-162">Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c232-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="1c232-163">Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c232-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="1c232-164">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1c232-164">Values of the xsd:string type.</span></span>  <br/> |
   

