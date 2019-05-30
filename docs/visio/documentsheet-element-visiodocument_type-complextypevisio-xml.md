---
title: DocumentSheet-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Gibt eine DocumentSheet-Struktur an.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540042"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="c55fe-103">DocumentSheet-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c55fe-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c55fe-104">Gibt eine DocumentSheet-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="c55fe-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c55fe-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c55fe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c55fe-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c55fe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c55fe-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c55fe-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c55fe-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c55fe-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c55fe-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c55fe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c55fe-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c55fe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c55fe-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="c55fe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c55fe-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="c55fe-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c55fe-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c55fe-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c55fe-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c55fe-114">Elements and attributes</span></span>

<span data-ttu-id="c55fe-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c55fe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c55fe-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c55fe-116">Parent elements</span></span>

|<span data-ttu-id="c55fe-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c55fe-117">**Element**</span></span>|<span data-ttu-id="c55fe-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c55fe-118">**Type**</span></span>|<span data-ttu-id="c55fe-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c55fe-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c55fe-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="c55fe-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="c55fe-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="c55fe-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c55fe-122">Das Stammelement eines Microsoft Visio Dokuments.</span><span class="sxs-lookup"><span data-stu-id="c55fe-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c55fe-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c55fe-123">Child elements</span></span>

|<span data-ttu-id="c55fe-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c55fe-124">**Element**</span></span>|<span data-ttu-id="c55fe-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c55fe-125">**Type**</span></span>|<span data-ttu-id="c55fe-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c55fe-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c55fe-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c55fe-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="c55fe-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c55fe-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c55fe-129">Gibt eine Zelle in einer DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="c55fe-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c55fe-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="c55fe-130">Attributes</span></span>

|<span data-ttu-id="c55fe-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c55fe-131">**Attribute**</span></span>|<span data-ttu-id="c55fe-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c55fe-132">**Type**</span></span>|<span data-ttu-id="c55fe-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c55fe-133">**Required**</span></span>|<span data-ttu-id="c55fe-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c55fe-134">**Description**</span></span>|<span data-ttu-id="c55fe-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c55fe-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c55fe-136">Iscustomname</span><span class="sxs-lookup"><span data-stu-id="c55fe-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="c55fe-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c55fe-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c55fe-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c55fe-138">optional</span></span>  <br/> |<span data-ttu-id="c55fe-139">Beschreibt, ob der Name vom Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="c55fe-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="c55fe-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="c55fe-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="c55fe-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c55fe-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c55fe-142">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c55fe-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c55fe-143">Optional</span><span class="sxs-lookup"><span data-stu-id="c55fe-143">optional</span></span>  <br/> |<span data-ttu-id="c55fe-144">Beschreibt, ob der universelle Name vom Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="c55fe-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="c55fe-145">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="c55fe-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="c55fe-146">Name</span><span class="sxs-lookup"><span data-stu-id="c55fe-146">Name</span></span>  <br/> |<span data-ttu-id="c55fe-147">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c55fe-147">xsd:string</span></span>  <br/> |<span data-ttu-id="c55fe-148">Optional</span><span class="sxs-lookup"><span data-stu-id="c55fe-148">optional</span></span>  <br/> |<span data-ttu-id="c55fe-149">Gibt den sprachabhängigen Namen des DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="c55fe-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="c55fe-150">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c55fe-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c55fe-151">NameU</span><span class="sxs-lookup"><span data-stu-id="c55fe-151">NameU</span></span>  <br/> |<span data-ttu-id="c55fe-152">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c55fe-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c55fe-153">Optional</span><span class="sxs-lookup"><span data-stu-id="c55fe-153">optional</span></span>  <br/> |<span data-ttu-id="c55fe-154">Gibt den sprachunabhängigen Namen des DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="c55fe-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="c55fe-155">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c55fe-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c55fe-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c55fe-156">UniqueID</span></span>  <br/> |<span data-ttu-id="c55fe-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c55fe-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c55fe-158">Optional</span><span class="sxs-lookup"><span data-stu-id="c55fe-158">optional</span></span>  <br/> |<span data-ttu-id="c55fe-159">Optionaler string-Wert.</span><span class="sxs-lookup"><span data-stu-id="c55fe-159">Optional string.</span></span> <span data-ttu-id="c55fe-160">Eine GUID (Globally Unique Identifier), die das Shape identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c55fe-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="c55fe-161">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c55fe-161">Values of the xsd:string type.</span></span>  <br/> |
   

