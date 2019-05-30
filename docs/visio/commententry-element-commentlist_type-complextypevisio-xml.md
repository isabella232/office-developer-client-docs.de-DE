---
title: CommentEntry-Element (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Gibt Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540112"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="4a81b-103">CommentEntry-Element (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4a81b-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4a81b-104">Gibt Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a81b-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a81b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4a81b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a81b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="4a81b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4a81b-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="4a81b-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4a81b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4a81b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4a81b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="4a81b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4a81b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4a81b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4a81b-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="4a81b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4a81b-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="4a81b-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a81b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="4a81b-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a81b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="4a81b-114">Elements and attributes</span></span>

<span data-ttu-id="4a81b-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="4a81b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4a81b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a81b-116">Parent elements</span></span>

|<span data-ttu-id="4a81b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a81b-117">**Element**</span></span>|<span data-ttu-id="4a81b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4a81b-118">**Type**</span></span>|<span data-ttu-id="4a81b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a81b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4a81b-120">Kommentarliste</span><span class="sxs-lookup"><span data-stu-id="4a81b-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4a81b-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="4a81b-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4a81b-122">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="4a81b-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4a81b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a81b-123">Child elements</span></span>

<span data-ttu-id="4a81b-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a81b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a81b-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="4a81b-125">Attributes</span></span>

|<span data-ttu-id="4a81b-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4a81b-126">**Attribute**</span></span>|<span data-ttu-id="4a81b-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="4a81b-127">**Type**</span></span>|<span data-ttu-id="4a81b-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="4a81b-128">**Required**</span></span>|<span data-ttu-id="4a81b-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a81b-129">**Description**</span></span>|<span data-ttu-id="4a81b-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="4a81b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a81b-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="4a81b-131">AuthorID</span></span>  <br/> |<span data-ttu-id="4a81b-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4a81b-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4a81b-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4a81b-133">required</span></span>  <br/> |<span data-ttu-id="4a81b-134">Ein 1-basierter Wert, der den Autor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a81b-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="4a81b-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="4a81b-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4a81b-136">Kommentar-Nr</span><span class="sxs-lookup"><span data-stu-id="4a81b-136">CommentID</span></span>  <br/> |<span data-ttu-id="4a81b-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4a81b-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4a81b-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4a81b-138">required</span></span>  <br/> |<span data-ttu-id="4a81b-139">Ein eindeutiger Wert, der den Kommentar auf einem Zeichenblatt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a81b-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="4a81b-140">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="4a81b-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4a81b-141">Datum</span><span class="sxs-lookup"><span data-stu-id="4a81b-141">Date</span></span>  <br/> |<span data-ttu-id="4a81b-142">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="4a81b-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4a81b-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4a81b-143">required</span></span>  <br/> |<span data-ttu-id="4a81b-144">Gibt an, wann ein Kommentar erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a81b-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="4a81b-145">Werte des Typs XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="4a81b-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4a81b-146">Fertig</span><span class="sxs-lookup"><span data-stu-id="4a81b-146">Done</span></span>  <br/> |<span data-ttu-id="4a81b-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4a81b-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4a81b-148">Optional</span><span class="sxs-lookup"><span data-stu-id="4a81b-148">optional</span></span>  <br/> |<span data-ttu-id="4a81b-149">Gibt den aktuellen Status des Kommentars an.</span><span class="sxs-lookup"><span data-stu-id="4a81b-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="4a81b-150">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="4a81b-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4a81b-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="4a81b-151">EditDate</span></span>  <br/> |<span data-ttu-id="4a81b-152">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="4a81b-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4a81b-153">Optional</span><span class="sxs-lookup"><span data-stu-id="4a81b-153">optional</span></span>  <br/> |<span data-ttu-id="4a81b-154">Gibt an, wann ein Kommentar zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a81b-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="4a81b-155">Werte des Typs XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="4a81b-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4a81b-156">PageID</span><span class="sxs-lookup"><span data-stu-id="4a81b-156">PageID</span></span>  <br/> |<span data-ttu-id="4a81b-157">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4a81b-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4a81b-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="4a81b-158">required</span></span>  <br/> |<span data-ttu-id="4a81b-159">Ein Wert, der das Zeichenblatt angibt, auf dem sich der Kommentar befindet.</span><span class="sxs-lookup"><span data-stu-id="4a81b-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="4a81b-160">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="4a81b-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4a81b-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="4a81b-161">ShapeID</span></span>  <br/> |<span data-ttu-id="4a81b-162">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4a81b-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4a81b-163">Optional</span><span class="sxs-lookup"><span data-stu-id="4a81b-163">optional</span></span>  <br/> |<span data-ttu-id="4a81b-164">Ein Wert, der die Form angibt, in der sich der Kommentar befindet.</span><span class="sxs-lookup"><span data-stu-id="4a81b-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="4a81b-165">Wenn keine Shape-Wert angegeben ist, bezieht sich der Kommentar auf das Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="4a81b-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="4a81b-166">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="4a81b-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

