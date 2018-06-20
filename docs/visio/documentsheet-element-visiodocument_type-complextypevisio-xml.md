---
title: DocumentSheet-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Gibt eine DocumentSheet-Struktur an.
ms.openlocfilehash: 50332759ff3bbe94887371d48c4a2e729243fb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796898"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="4312d-103">DocumentSheet-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="4312d-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4312d-104">Gibt eine DocumentSheet-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="4312d-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4312d-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4312d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4312d-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4312d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4312d-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4312d-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4312d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4312d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4312d-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4312d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4312d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4312d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4312d-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="4312d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4312d-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="4312d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4312d-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4312d-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4312d-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4312d-114">Elements and attributes</span></span>

<span data-ttu-id="4312d-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="4312d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4312d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4312d-116">Parent elements</span></span>

|<span data-ttu-id="4312d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4312d-117">**Element**</span></span>|<span data-ttu-id="4312d-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4312d-118">**Type**</span></span>|<span data-ttu-id="4312d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4312d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4312d-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="4312d-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="4312d-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4312d-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4312d-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4312d-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4312d-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4312d-123">Child elements</span></span>

|<span data-ttu-id="4312d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4312d-124">**Element**</span></span>|<span data-ttu-id="4312d-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4312d-125">**Type**</span></span>|<span data-ttu-id="4312d-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4312d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4312d-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4312d-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="4312d-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4312d-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4312d-129">Gibt eine Zelle in einem DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="4312d-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4312d-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="4312d-130">Attributes</span></span>

|<span data-ttu-id="4312d-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4312d-131">**Attribute**</span></span>|<span data-ttu-id="4312d-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4312d-132">**Type**</span></span>|<span data-ttu-id="4312d-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4312d-133">**Required**</span></span>|<span data-ttu-id="4312d-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4312d-134">**Description**</span></span>|<span data-ttu-id="4312d-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4312d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4312d-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="4312d-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="4312d-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4312d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4312d-138">Optional</span><span class="sxs-lookup"><span data-stu-id="4312d-138">optional</span></span>  <br/> |<span data-ttu-id="4312d-139">Beschreibt, ob der Name des Benutzers angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="4312d-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="4312d-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4312d-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="4312d-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="4312d-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4312d-142">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4312d-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4312d-143">Optional</span><span class="sxs-lookup"><span data-stu-id="4312d-143">optional</span></span>  <br/> |<span data-ttu-id="4312d-144">Beschreibt, ob der universelle Name durch den Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="4312d-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="4312d-145">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4312d-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="4312d-146">Name</span><span class="sxs-lookup"><span data-stu-id="4312d-146">Name</span></span>  <br/> |<span data-ttu-id="4312d-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4312d-147">xsd:string</span></span>  <br/> |<span data-ttu-id="4312d-148">Optional</span><span class="sxs-lookup"><span data-stu-id="4312d-148">optional</span></span>  <br/> |<span data-ttu-id="4312d-149">Gibt den Namen der Sprache abhängig von der DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="4312d-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="4312d-150">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4312d-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4312d-151">NameU</span><span class="sxs-lookup"><span data-stu-id="4312d-151">NameU</span></span>  <br/> |<span data-ttu-id="4312d-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4312d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4312d-153">Optional</span><span class="sxs-lookup"><span data-stu-id="4312d-153">optional</span></span>  <br/> |<span data-ttu-id="4312d-154">Der sprachenunabhängige Name des die DocumentSheet gibt.</span><span class="sxs-lookup"><span data-stu-id="4312d-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="4312d-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4312d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4312d-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="4312d-156">UniqueID</span></span>  <br/> |<span data-ttu-id="4312d-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4312d-157">xsd:string</span></span>  <br/> |<span data-ttu-id="4312d-158">Optional</span><span class="sxs-lookup"><span data-stu-id="4312d-158">optional</span></span>  <br/> |<span data-ttu-id="4312d-159">Optionaler String-Wert.</span><span class="sxs-lookup"><span data-stu-id="4312d-159">Optional string.</span></span> <span data-ttu-id="4312d-160">Eine GUID (globally unique Identifier), die das Shape identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4312d-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="4312d-161">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4312d-161">Values of the xsd:string type.</span></span>  <br/> |
   

