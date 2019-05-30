---
title: AuthorEntry-Element (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt Eigenschaften an, mit denen der Autor eines Kommentars in einer Zeichnung identifiziert wird.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537906"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="6ebcd-103">AuthorEntry-Element (AuthorList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6ebcd-103">AuthorEntry element (AuthorList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6ebcd-104">Gibt Eigenschaften an, mit denen der Autor eines Kommentars in einer Zeichnung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ebcd-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6ebcd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ebcd-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6ebcd-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="6ebcd-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6ebcd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6ebcd-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6ebcd-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6ebcd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6ebcd-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6ebcd-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="6ebcd-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ebcd-113">Definition</span><span class="sxs-lookup"><span data-stu-id="6ebcd-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ebcd-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6ebcd-114">Elements and attributes</span></span>

<span data-ttu-id="6ebcd-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6ebcd-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ebcd-116">Parent elements</span></span>

|<span data-ttu-id="6ebcd-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-117">**Element**</span></span>|<span data-ttu-id="6ebcd-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-118">**Type**</span></span>|<span data-ttu-id="6ebcd-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ebcd-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="6ebcd-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ebcd-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="6ebcd-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ebcd-122">Gibt die Autoren in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ebcd-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ebcd-123">Child elements</span></span>

<span data-ttu-id="6ebcd-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ebcd-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ebcd-125">Attributes</span></span>

|<span data-ttu-id="6ebcd-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-126">**Attribute**</span></span>|<span data-ttu-id="6ebcd-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-127">**Type**</span></span>|<span data-ttu-id="6ebcd-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-128">**Required**</span></span>|<span data-ttu-id="6ebcd-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-129">**Description**</span></span>|<span data-ttu-id="6ebcd-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6ebcd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6ebcd-131">ID</span><span class="sxs-lookup"><span data-stu-id="6ebcd-131">ID</span></span>  <br/> |<span data-ttu-id="6ebcd-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ebcd-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6ebcd-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6ebcd-133">required</span></span>  <br/> |<span data-ttu-id="6ebcd-134">Ein 1-basierter Wert, der den Autor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="6ebcd-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6ebcd-136">Initialen</span><span class="sxs-lookup"><span data-stu-id="6ebcd-136">Initials</span></span>  <br/> |<span data-ttu-id="6ebcd-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ebcd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6ebcd-138">Optional</span><span class="sxs-lookup"><span data-stu-id="6ebcd-138">optional</span></span>  <br/> |<span data-ttu-id="6ebcd-139">Die Initialen des Autors.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="6ebcd-140">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6ebcd-141">Name</span><span class="sxs-lookup"><span data-stu-id="6ebcd-141">Name</span></span>  <br/> |<span data-ttu-id="6ebcd-142">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ebcd-142">xsd:string</span></span>  <br/> |<span data-ttu-id="6ebcd-143">Optional</span><span class="sxs-lookup"><span data-stu-id="6ebcd-143">optional</span></span>  <br/> |<span data-ttu-id="6ebcd-144">Der Name des Autors.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="6ebcd-145">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6ebcd-146">Resolutional</span><span class="sxs-lookup"><span data-stu-id="6ebcd-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="6ebcd-147">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ebcd-147">xsd:string</span></span>  <br/> |<span data-ttu-id="6ebcd-148">Optional</span><span class="sxs-lookup"><span data-stu-id="6ebcd-148">optional</span></span>  <br/> |<span data-ttu-id="6ebcd-149">Ein eindeutiger Bezeichner für den Autor.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="6ebcd-150">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-150">Values of the xsd:string type.</span></span>  <br/> |
   

