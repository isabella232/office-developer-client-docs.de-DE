---
title: AuthorEntry-Element (AuthorList_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt Eigenschaften verwendet, um den Autor eines Kommentars in einer Zeichnung zu ermitteln.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796412"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="3079a-103">AuthorEntry-Element (AuthorList_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3079a-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3079a-104">Gibt Eigenschaften verwendet, um den Autor eines Kommentars in einer Zeichnung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="3079a-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3079a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3079a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3079a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3079a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3079a-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3079a-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3079a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3079a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3079a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3079a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3079a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3079a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3079a-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="3079a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3079a-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="3079a-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3079a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="3079a-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3079a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3079a-114">Elements and attributes</span></span>

<span data-ttu-id="3079a-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3079a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3079a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3079a-116">Parent elements</span></span>

|<span data-ttu-id="3079a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3079a-117">**Element**</span></span>|<span data-ttu-id="3079a-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3079a-118">**Type**</span></span>|<span data-ttu-id="3079a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3079a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3079a-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="3079a-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3079a-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="3079a-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3079a-122">Gibt die Autoren in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="3079a-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3079a-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3079a-123">Child elements</span></span>

<span data-ttu-id="3079a-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="3079a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3079a-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="3079a-125">Attributes</span></span>

|<span data-ttu-id="3079a-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3079a-126">**Attribute**</span></span>|<span data-ttu-id="3079a-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3079a-127">**Type**</span></span>|<span data-ttu-id="3079a-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3079a-128">**Required**</span></span>|<span data-ttu-id="3079a-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3079a-129">**Description**</span></span>|<span data-ttu-id="3079a-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3079a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3079a-131">ID</span><span class="sxs-lookup"><span data-stu-id="3079a-131">ID</span></span>  <br/> |<span data-ttu-id="3079a-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3079a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3079a-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3079a-133">required</span></span>  <br/> |<span data-ttu-id="3079a-134">Ein 1-basierte Wert, der Autor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3079a-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="3079a-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3079a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3079a-136">Initialen</span><span class="sxs-lookup"><span data-stu-id="3079a-136">Initials</span></span>  <br/> |<span data-ttu-id="3079a-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3079a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3079a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="3079a-138">optional</span></span>  <br/> |<span data-ttu-id="3079a-139">Die Initialen des Autors.</span><span class="sxs-lookup"><span data-stu-id="3079a-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="3079a-140">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3079a-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3079a-141">Name</span><span class="sxs-lookup"><span data-stu-id="3079a-141">Name</span></span>  <br/> |<span data-ttu-id="3079a-142">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3079a-142">xsd:string</span></span>  <br/> |<span data-ttu-id="3079a-143">Optional</span><span class="sxs-lookup"><span data-stu-id="3079a-143">optional</span></span>  <br/> |<span data-ttu-id="3079a-144">Der Name des Autors.</span><span class="sxs-lookup"><span data-stu-id="3079a-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="3079a-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3079a-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3079a-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="3079a-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="3079a-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3079a-147">xsd:string</span></span>  <br/> |<span data-ttu-id="3079a-148">Optional</span><span class="sxs-lookup"><span data-stu-id="3079a-148">optional</span></span>  <br/> |<span data-ttu-id="3079a-149">Ein eindeutiger Bezeichner für den Autor.</span><span class="sxs-lookup"><span data-stu-id="3079a-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="3079a-150">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3079a-150">Values of the xsd:string type.</span></span>  <br/> |
   

