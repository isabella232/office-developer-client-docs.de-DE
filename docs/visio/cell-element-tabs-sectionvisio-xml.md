---
title: Zellenelement (Abschnitt "Tabs") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: Gibt eine Eigenschaft, die Form und-Art Tabstoppposition oder Ausrichtung von Steuerelementen an.
ms.openlocfilehash: da2fb31688227180bb38a4366c3293a2e16600c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796605"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="ad7ec-103">Zellenelement (Abschnitt "Tabs") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ad7ec-103">Cell element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="ad7ec-104">Gibt eine Eigenschaft, die Form und-Art Tabstoppposition oder Ausrichtung von Steuerelementen an.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ad7ec-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ad7ec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad7ec-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad7ec-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ad7ec-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad7ec-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad7ec-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad7ec-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad7ec-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad7ec-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad7ec-112">Document.XML, master # .xml, Seite # .xml</span><span class="sxs-lookup"><span data-stu-id="ad7ec-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad7ec-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ad7ec-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad7ec-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ad7ec-114">Elements and attributes</span></span>

<span data-ttu-id="ad7ec-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad7ec-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad7ec-116">Parent elements</span></span>

|<span data-ttu-id="ad7ec-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-117">**Element**</span></span>|<span data-ttu-id="ad7ec-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-118">**Type**</span></span>|<span data-ttu-id="ad7ec-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad7ec-120">Zeilenelement (Tabs-Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="ad7ec-120">Row element (Tabs Section)</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ad7ec-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="ad7ec-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad7ec-122">Gibt eine Eigenschaft, die Form und-Art Tabstoppposition oder Ausrichtung von Steuerelementen an.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad7ec-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad7ec-123">Child elements</span></span>

|<span data-ttu-id="ad7ec-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-124">**Element**</span></span>|<span data-ttu-id="ad7ec-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-125">**Type**</span></span>|<span data-ttu-id="ad7ec-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad7ec-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="ad7ec-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad7ec-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ad7ec-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad7ec-129">Gibt einen Verweis auf ein Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad7ec-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad7ec-130">Attributes</span></span>

|<span data-ttu-id="ad7ec-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-131">**Attribute**</span></span>|<span data-ttu-id="ad7ec-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-132">**Type**</span></span>|<span data-ttu-id="ad7ec-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-133">**Required**</span></span>|<span data-ttu-id="ad7ec-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-134">**Description**</span></span>|<span data-ttu-id="ad7ec-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad7ec-136">E</span><span class="sxs-lookup"><span data-stu-id="ad7ec-136">E</span></span>  <br/> |<span data-ttu-id="ad7ec-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ad7ec-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ec-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ad7ec-138">optional</span></span>  <br/> |<span data-ttu-id="ad7ec-139">Gibt an, dass die Formel einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="ad7ec-140">Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="ad7ec-141">Zeichenfolge mit einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="ad7ec-142">F</span><span class="sxs-lookup"><span data-stu-id="ad7ec-142">F</span></span>  <br/> |<span data-ttu-id="ad7ec-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ad7ec-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ec-144">Optional</span><span class="sxs-lookup"><span data-stu-id="ad7ec-144">optional</span></span>  <br/> | <span data-ttu-id="ad7ec-145">Formel für das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-145">Represents the element's formula.</span></span> <span data-ttu-id="ad7ec-146">Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="ad7ec-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="ad7ec-147">"(einige Formel)" Wenn die Formel lokal vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="ad7ec-148">`No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="ad7ec-149">`Inh`Wenn die Formel geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="ad7ec-150">Eine Formel.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="ad7ec-151">N</span><span class="sxs-lookup"><span data-stu-id="ad7ec-151">N</span></span>  <br/> |<span data-ttu-id="ad7ec-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ad7ec-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ec-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ad7ec-153">required</span></span>  <br/> |<span data-ttu-id="ad7ec-154">Der Name der ShapeSheet-Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="ad7ec-155">Der Name der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="ad7ec-156">Siehe Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ad7ec-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="ad7ec-157">U</span><span class="sxs-lookup"><span data-stu-id="ad7ec-157">U</span></span>  <br/> |<span data-ttu-id="ad7ec-158">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ad7ec-158">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ec-159">Optional</span><span class="sxs-lookup"><span data-stu-id="ad7ec-159">optional</span></span>  <br/> |<span data-ttu-id="ad7ec-160">Stellt eine Einheit der Messung der Standardwert ist DL.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="ad7ec-161">Die Einheiten der Zelle.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="ad7ec-162">V</span><span class="sxs-lookup"><span data-stu-id="ad7ec-162">V</span></span>  <br/> |<span data-ttu-id="ad7ec-163">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ad7ec-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ad7ec-164">Optional</span><span class="sxs-lookup"><span data-stu-id="ad7ec-164">optional</span></span>  <br/> |<span data-ttu-id="ad7ec-165">Den Wert der Zelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="ad7ec-166">Der Wert der ShapeSheet-Zelle.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad7ec-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad7ec-167">Remarks</span></span>

<span data-ttu-id="ad7ec-168">Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="ad7ec-169">Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="ad7ec-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-170">**Value**</span></span>|<span data-ttu-id="ad7ec-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-171">**Description**</span></span>|<span data-ttu-id="ad7ec-172">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="ad7ec-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad7ec-173">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="ad7ec-173">Alignment</span></span>  <br/> |<span data-ttu-id="ad7ec-174">Legt die Tabausrichtung fest.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-174">Specifies the tab alignment.</span></span>  <br/> |[<span data-ttu-id="ad7ec-175">Zelle "Alignment" (Abschnitt "Tabs")</span><span class="sxs-lookup"><span data-stu-id="ad7ec-175">Alignment Cell (Tabs Section)</span></span>](alignment-cell-tabs-section.md) <br/> |
|<span data-ttu-id="ad7ec-176">Position</span><span class="sxs-lookup"><span data-stu-id="ad7ec-176">Position</span></span>  <br/> |<span data-ttu-id="ad7ec-p104">Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.</span><span class="sxs-lookup"><span data-stu-id="ad7ec-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |[<span data-ttu-id="ad7ec-180">Zelle "Position" (Abschnitt "Tabs")</span><span class="sxs-lookup"><span data-stu-id="ad7ec-180">Position Cell (Tabs Section)</span></span>](position-cell-tabs-section.md) <br/> |
   

