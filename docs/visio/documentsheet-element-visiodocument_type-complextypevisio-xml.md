---
title: DocumentSheet-Element (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Gibt eine DocumentSheet-Struktur an.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356364"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ba7a9-103">DocumentSheet-Element (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ba7a9-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ba7a9-104">Gibt eine DocumentSheet-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba7a9-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ba7a9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba7a9-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ba7a9-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ba7a9-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ba7a9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ba7a9-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ba7a9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ba7a9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ba7a9-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ba7a9-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="ba7a9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ba7a9-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ba7a9-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ba7a9-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ba7a9-114">Elements and attributes</span></span>

<span data-ttu-id="ba7a9-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ba7a9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba7a9-116">Parent elements</span></span>

|<span data-ttu-id="ba7a9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-117">**Element**</span></span>|<span data-ttu-id="ba7a9-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-118">**Type**</span></span>|<span data-ttu-id="ba7a9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ba7a9-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ba7a9-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ba7a9-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ba7a9-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ba7a9-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ba7a9-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba7a9-123">Child elements</span></span>

|<span data-ttu-id="ba7a9-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-124">**Element**</span></span>|<span data-ttu-id="ba7a9-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-125">**Type**</span></span>|<span data-ttu-id="ba7a9-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ba7a9-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ba7a9-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="ba7a9-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ba7a9-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ba7a9-129">Gibt eine Zelle in einem DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ba7a9-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba7a9-130">Attributes</span></span>

|<span data-ttu-id="ba7a9-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-131">**Attribute**</span></span>|<span data-ttu-id="ba7a9-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-132">**Type**</span></span>|<span data-ttu-id="ba7a9-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-133">**Required**</span></span>|<span data-ttu-id="ba7a9-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-134">**Description**</span></span>|<span data-ttu-id="ba7a9-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ba7a9-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ba7a9-136">IsCustomname</span><span class="sxs-lookup"><span data-stu-id="ba7a9-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="ba7a9-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ba7a9-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ba7a9-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ba7a9-138">optional</span></span>  <br/> |<span data-ttu-id="ba7a9-139">Beschreibt, ob der Name vom Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="ba7a9-140">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="ba7a9-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="ba7a9-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ba7a9-142">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ba7a9-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ba7a9-143">Optional</span><span class="sxs-lookup"><span data-stu-id="ba7a9-143">optional</span></span>  <br/> |<span data-ttu-id="ba7a9-144">Beschreibt, ob der universelle Name vom Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="ba7a9-145">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="ba7a9-146">Name</span><span class="sxs-lookup"><span data-stu-id="ba7a9-146">Name</span></span>  <br/> |<span data-ttu-id="ba7a9-147">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ba7a9-147">xsd:string</span></span>  <br/> |<span data-ttu-id="ba7a9-148">Optional</span><span class="sxs-lookup"><span data-stu-id="ba7a9-148">optional</span></span>  <br/> |<span data-ttu-id="ba7a9-149">Gibt den sprachabhängigen Namen des DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="ba7a9-150">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ba7a9-151">NameU</span><span class="sxs-lookup"><span data-stu-id="ba7a9-151">NameU</span></span>  <br/> |<span data-ttu-id="ba7a9-152">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ba7a9-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ba7a9-153">Optional</span><span class="sxs-lookup"><span data-stu-id="ba7a9-153">optional</span></span>  <br/> |<span data-ttu-id="ba7a9-154">Gibt den sprachunabhängigen Namen des DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="ba7a9-155">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ba7a9-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ba7a9-156">UniqueID</span></span>  <br/> |<span data-ttu-id="ba7a9-157">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ba7a9-157">xsd:string</span></span>  <br/> |<span data-ttu-id="ba7a9-158">Optional</span><span class="sxs-lookup"><span data-stu-id="ba7a9-158">optional</span></span>  <br/> |<span data-ttu-id="ba7a9-159">Optionaler string-Wert.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-159">Optional string.</span></span> <span data-ttu-id="ba7a9-160">Eine GUID (Globally Unique Identifier), die die Form identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="ba7a9-161">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-161">Values of the xsd:string type.</span></span>  <br/> |
   

