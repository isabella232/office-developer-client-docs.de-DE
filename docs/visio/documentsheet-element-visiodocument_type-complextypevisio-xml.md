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
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="30753-103">DocumentSheet-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="30753-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="30753-104">Gibt eine DocumentSheet-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="30753-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30753-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="30753-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30753-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="30753-106">**Element type**</span></span> <br/> |[<span data-ttu-id="30753-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="30753-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="30753-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30753-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="30753-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="30753-109">**Schema file**</span></span> <br/> |<span data-ttu-id="30753-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="30753-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="30753-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="30753-111">**Document parts**</span></span> <br/> |<span data-ttu-id="30753-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="30753-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30753-113">Definition</span><span class="sxs-lookup"><span data-stu-id="30753-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="30753-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="30753-114">Elements and attributes</span></span>

<span data-ttu-id="30753-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="30753-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="30753-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30753-116">Parent elements</span></span>

|<span data-ttu-id="30753-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="30753-117">**Element**</span></span>|<span data-ttu-id="30753-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="30753-118">**Type**</span></span>|<span data-ttu-id="30753-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30753-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30753-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="30753-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="30753-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="30753-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30753-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="30753-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="30753-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30753-123">Child elements</span></span>

|<span data-ttu-id="30753-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="30753-124">**Element**</span></span>|<span data-ttu-id="30753-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="30753-125">**Type**</span></span>|<span data-ttu-id="30753-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30753-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30753-127">Cell</span><span class="sxs-lookup"><span data-stu-id="30753-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="30753-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="30753-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30753-129">Gibt eine Zelle in einem DocumentSheet an.</span><span class="sxs-lookup"><span data-stu-id="30753-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="30753-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="30753-130">Attributes</span></span>

|<span data-ttu-id="30753-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="30753-131">**Attribute**</span></span>|<span data-ttu-id="30753-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="30753-132">**Type**</span></span>|<span data-ttu-id="30753-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="30753-133">**Required**</span></span>|<span data-ttu-id="30753-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30753-134">**Description**</span></span>|<span data-ttu-id="30753-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="30753-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30753-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="30753-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="30753-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="30753-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="30753-138">Optional</span><span class="sxs-lookup"><span data-stu-id="30753-138">optional</span></span>  <br/> |<span data-ttu-id="30753-139">Beschreibt, ob der Name des Benutzers angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="30753-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="30753-140">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="30753-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="30753-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="30753-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="30753-142">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="30753-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="30753-143">Optional</span><span class="sxs-lookup"><span data-stu-id="30753-143">optional</span></span>  <br/> |<span data-ttu-id="30753-144">Beschreibt, ob der universelle Name durch den Benutzer angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="30753-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="30753-145">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="30753-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="30753-146">Name</span><span class="sxs-lookup"><span data-stu-id="30753-146">Name</span></span>  <br/> |<span data-ttu-id="30753-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="30753-147">xsd:string</span></span>  <br/> |<span data-ttu-id="30753-148">Optional</span><span class="sxs-lookup"><span data-stu-id="30753-148">optional</span></span>  <br/> |<span data-ttu-id="30753-149">Gibt den Namen der Sprache abhängig von der DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="30753-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="30753-150">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30753-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="30753-151">NameU</span><span class="sxs-lookup"><span data-stu-id="30753-151">NameU</span></span>  <br/> |<span data-ttu-id="30753-152">XSD: String</span><span class="sxs-lookup"><span data-stu-id="30753-152">xsd:string</span></span>  <br/> |<span data-ttu-id="30753-153">Optional</span><span class="sxs-lookup"><span data-stu-id="30753-153">optional</span></span>  <br/> |<span data-ttu-id="30753-154">Der sprachenunabhängige Name des die DocumentSheet gibt.</span><span class="sxs-lookup"><span data-stu-id="30753-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="30753-155">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30753-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="30753-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="30753-156">UniqueID</span></span>  <br/> |<span data-ttu-id="30753-157">XSD: String</span><span class="sxs-lookup"><span data-stu-id="30753-157">xsd:string</span></span>  <br/> |<span data-ttu-id="30753-158">Optional</span><span class="sxs-lookup"><span data-stu-id="30753-158">optional</span></span>  <br/> |<span data-ttu-id="30753-159">Optionaler string-Wert.</span><span class="sxs-lookup"><span data-stu-id="30753-159">Optional string.</span></span> <span data-ttu-id="30753-160">Eine GUID (globally unique Identifier), die das Shape identifiziert.</span><span class="sxs-lookup"><span data-stu-id="30753-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="30753-161">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30753-161">Values of the xsd:string type.</span></span>  <br/> |
   

