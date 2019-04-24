---
title: AuthorEntry-Element (AuthorList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt die Eigenschaften an, die zum Identifizieren des Autors eines Kommentars in einer Zeichnung verwendet werden.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338626"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="d327d-103">AuthorEntry-Element (AuthorList_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d327d-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d327d-104">Gibt die Eigenschaften an, die zum Identifizieren des Autors eines Kommentars in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d327d-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d327d-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d327d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d327d-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d327d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d327d-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="d327d-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d327d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d327d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d327d-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d327d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d327d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d327d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d327d-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="d327d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d327d-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="d327d-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d327d-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d327d-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d327d-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d327d-114">Elements and attributes</span></span>

<span data-ttu-id="d327d-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d327d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d327d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d327d-116">Parent elements</span></span>

|<span data-ttu-id="d327d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d327d-117">**Element**</span></span>|<span data-ttu-id="d327d-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d327d-118">**Type**</span></span>|<span data-ttu-id="d327d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d327d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d327d-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="d327d-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d327d-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="d327d-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d327d-122">Gibt die Autoren in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="d327d-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d327d-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d327d-123">Child elements</span></span>

<span data-ttu-id="d327d-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="d327d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d327d-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d327d-125">Attributes</span></span>

|<span data-ttu-id="d327d-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d327d-126">**Attribute**</span></span>|<span data-ttu-id="d327d-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d327d-127">**Type**</span></span>|<span data-ttu-id="d327d-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d327d-128">**Required**</span></span>|<span data-ttu-id="d327d-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d327d-129">**Description**</span></span>|<span data-ttu-id="d327d-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d327d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d327d-131">ID</span><span class="sxs-lookup"><span data-stu-id="d327d-131">ID</span></span>  <br/> |<span data-ttu-id="d327d-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d327d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d327d-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d327d-133">required</span></span>  <br/> |<span data-ttu-id="d327d-134">Ein 1-basierter Wert, der den Autor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d327d-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="d327d-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="d327d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d327d-136">Initialen</span><span class="sxs-lookup"><span data-stu-id="d327d-136">Initials</span></span>  <br/> |<span data-ttu-id="d327d-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d327d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d327d-138">Optional</span><span class="sxs-lookup"><span data-stu-id="d327d-138">optional</span></span>  <br/> |<span data-ttu-id="d327d-139">Die Initialen des Autors.</span><span class="sxs-lookup"><span data-stu-id="d327d-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="d327d-140">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="d327d-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d327d-141">Name</span><span class="sxs-lookup"><span data-stu-id="d327d-141">Name</span></span>  <br/> |<span data-ttu-id="d327d-142">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d327d-142">xsd:string</span></span>  <br/> |<span data-ttu-id="d327d-143">Optional</span><span class="sxs-lookup"><span data-stu-id="d327d-143">optional</span></span>  <br/> |<span data-ttu-id="d327d-144">Der Name des Autors.</span><span class="sxs-lookup"><span data-stu-id="d327d-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="d327d-145">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="d327d-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d327d-146">Lösungs-Nr</span><span class="sxs-lookup"><span data-stu-id="d327d-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="d327d-147">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d327d-147">xsd:string</span></span>  <br/> |<span data-ttu-id="d327d-148">Optional</span><span class="sxs-lookup"><span data-stu-id="d327d-148">optional</span></span>  <br/> |<span data-ttu-id="d327d-149">Ein eindeutiger Bezeichner für den Autor.</span><span class="sxs-lookup"><span data-stu-id="d327d-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="d327d-150">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="d327d-150">Values of the xsd:string type.</span></span>  <br/> |
   

