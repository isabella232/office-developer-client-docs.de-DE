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
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="80b25-103">DocumentSheet-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="80b25-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="80b25-104">Gibt eine DocumentSheet-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="80b25-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80b25-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="80b25-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80b25-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="80b25-106">**Element type**</span></span> <br/> |[<span data-ttu-id="80b25-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="80b25-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="80b25-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="80b25-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="80b25-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="80b25-109">**Schema file**</span></span> <br/> |<span data-ttu-id="80b25-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="80b25-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="80b25-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="80b25-111">**Document parts**</span></span> <br/> |<span data-ttu-id="80b25-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="80b25-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80b25-113">Definition</span><span class="sxs-lookup"><span data-stu-id="80b25-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="80b25-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="80b25-114">Elements and attributes</span></span>

<span data-ttu-id="80b25-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="80b25-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="80b25-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80b25-116">Parent elements</span></span>

|<span data-ttu-id="80b25-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="80b25-117">**Element**</span></span>|<span data-ttu-id="80b25-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="80b25-118">**Type**</span></span>|<span data-ttu-id="80b25-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80b25-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="80b25-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="80b25-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="80b25-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="80b25-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="80b25-122">Das Stammelement eines Microsoft-Visio Dokument.</span><span class="sxs-lookup"><span data-stu-id="80b25-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="80b25-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80b25-123">Child elements</span></span>

|<span data-ttu-id="80b25-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="80b25-124">**Element**</span></span>|<span data-ttu-id="80b25-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="80b25-125">**Type**</span></span>|<span data-ttu-id="80b25-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80b25-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="80b25-127">Cell</span><span class="sxs-lookup"><span data-stu-id="80b25-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="80b25-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="80b25-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="80b25-129">Gibt eine Zelle in einem DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="80b25-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="80b25-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="80b25-130">Attributes</span></span>

|<span data-ttu-id="80b25-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="80b25-131">**Attribute**</span></span>|<span data-ttu-id="80b25-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="80b25-132">**Type**</span></span>|<span data-ttu-id="80b25-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="80b25-133">**Required**</span></span>|<span data-ttu-id="80b25-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80b25-134">**Description**</span></span>|<span data-ttu-id="80b25-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="80b25-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80b25-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="80b25-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="80b25-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="80b25-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="80b25-138">Optional</span><span class="sxs-lookup"><span data-stu-id="80b25-138">optional</span></span>  <br/> |<span data-ttu-id="80b25-139">Beschreibt, ob der Name vom Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="80b25-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="80b25-140">Werte des xsd:Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="80b25-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="80b25-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="80b25-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="80b25-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="80b25-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="80b25-143">Optional</span><span class="sxs-lookup"><span data-stu-id="80b25-143">optional</span></span>  <br/> |<span data-ttu-id="80b25-144">Beschreibt, ob der universelle Name vom Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="80b25-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="80b25-145">Werte des xsd:Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="80b25-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="80b25-146">Name</span><span class="sxs-lookup"><span data-stu-id="80b25-146">Name</span></span>  <br/> |<span data-ttu-id="80b25-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="80b25-147">xsd:string</span></span>  <br/> |<span data-ttu-id="80b25-148">Optional</span><span class="sxs-lookup"><span data-stu-id="80b25-148">optional</span></span>  <br/> |<span data-ttu-id="80b25-149">Gibt den sprachabhängigen Namen des DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="80b25-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="80b25-150">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="80b25-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="80b25-151">NameU</span><span class="sxs-lookup"><span data-stu-id="80b25-151">NameU</span></span>  <br/> |<span data-ttu-id="80b25-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="80b25-152">xsd:string</span></span>  <br/> |<span data-ttu-id="80b25-153">Optional</span><span class="sxs-lookup"><span data-stu-id="80b25-153">optional</span></span>  <br/> |<span data-ttu-id="80b25-154">Gibt den sprachunabhängigen Namen des DocumentSheets an.</span><span class="sxs-lookup"><span data-stu-id="80b25-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="80b25-155">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="80b25-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="80b25-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="80b25-156">UniqueID</span></span>  <br/> |<span data-ttu-id="80b25-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="80b25-157">xsd:string</span></span>  <br/> |<span data-ttu-id="80b25-158">Optional</span><span class="sxs-lookup"><span data-stu-id="80b25-158">optional</span></span>  <br/> |<span data-ttu-id="80b25-159">Optionaler string-Wert.</span><span class="sxs-lookup"><span data-stu-id="80b25-159">Optional string.</span></span> <span data-ttu-id="80b25-160">Eine GUID (global eindeutiger Bezeichner), die das Shape identifiziert.</span><span class="sxs-lookup"><span data-stu-id="80b25-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="80b25-161">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="80b25-161">Values of the xsd:string type.</span></span>  <br/> |
   

