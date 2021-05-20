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
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="9dcae-103">CommentEntry-Element (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9dcae-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9dcae-104">Gibt Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dcae-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dcae-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9dcae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dcae-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9dcae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9dcae-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="9dcae-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9dcae-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9dcae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9dcae-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9dcae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9dcae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9dcae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9dcae-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="9dcae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9dcae-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="9dcae-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9dcae-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9dcae-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9dcae-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9dcae-114">Elements and attributes</span></span>

<span data-ttu-id="9dcae-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9dcae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9dcae-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9dcae-116">Parent elements</span></span>

|<span data-ttu-id="9dcae-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9dcae-117">**Element**</span></span>|<span data-ttu-id="9dcae-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9dcae-118">**Type**</span></span>|<span data-ttu-id="9dcae-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9dcae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dcae-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="9dcae-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9dcae-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="9dcae-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9dcae-122">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="9dcae-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9dcae-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9dcae-123">Child elements</span></span>

<span data-ttu-id="9dcae-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="9dcae-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9dcae-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="9dcae-125">Attributes</span></span>

|<span data-ttu-id="9dcae-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9dcae-126">**Attribute**</span></span>|<span data-ttu-id="9dcae-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9dcae-127">**Type**</span></span>|<span data-ttu-id="9dcae-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9dcae-128">**Required**</span></span>|<span data-ttu-id="9dcae-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9dcae-129">**Description**</span></span>|<span data-ttu-id="9dcae-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9dcae-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9dcae-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="9dcae-131">AuthorID</span></span>  <br/> |<span data-ttu-id="9dcae-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9dcae-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9dcae-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9dcae-133">required</span></span>  <br/> |<span data-ttu-id="9dcae-134">Ein einbasierter Wert, der den Autor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9dcae-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="9dcae-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9dcae-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9dcae-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="9dcae-136">CommentID</span></span>  <br/> |<span data-ttu-id="9dcae-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9dcae-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9dcae-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9dcae-138">required</span></span>  <br/> |<span data-ttu-id="9dcae-139">Ein eindeutiger Wert, der den Kommentar auf einem Zeichenblatt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9dcae-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="9dcae-140">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9dcae-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9dcae-141">Datum</span><span class="sxs-lookup"><span data-stu-id="9dcae-141">Date</span></span>  <br/> |<span data-ttu-id="9dcae-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="9dcae-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9dcae-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9dcae-143">required</span></span>  <br/> |<span data-ttu-id="9dcae-144">Gibt an, wann ein Kommentar erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9dcae-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="9dcae-145">Werte des xsd:dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="9dcae-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9dcae-146">Fertig</span><span class="sxs-lookup"><span data-stu-id="9dcae-146">Done</span></span>  <br/> |<span data-ttu-id="9dcae-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9dcae-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9dcae-148">Optional</span><span class="sxs-lookup"><span data-stu-id="9dcae-148">optional</span></span>  <br/> |<span data-ttu-id="9dcae-149">Gibt den aktuellen Status des Kommentars an.</span><span class="sxs-lookup"><span data-stu-id="9dcae-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="9dcae-150">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9dcae-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9dcae-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="9dcae-151">EditDate</span></span>  <br/> |<span data-ttu-id="9dcae-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="9dcae-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9dcae-153">Optional</span><span class="sxs-lookup"><span data-stu-id="9dcae-153">optional</span></span>  <br/> |<span data-ttu-id="9dcae-154">Gibt an, wann ein Kommentar zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9dcae-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="9dcae-155">Werte des xsd:dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="9dcae-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9dcae-156">PageID</span><span class="sxs-lookup"><span data-stu-id="9dcae-156">PageID</span></span>  <br/> |<span data-ttu-id="9dcae-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9dcae-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9dcae-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9dcae-158">required</span></span>  <br/> |<span data-ttu-id="9dcae-159">Ein Wert, der das Zeichenblatt identifiziert, auf dem sich der Kommentar befindet.</span><span class="sxs-lookup"><span data-stu-id="9dcae-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="9dcae-160">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9dcae-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9dcae-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="9dcae-161">ShapeID</span></span>  <br/> |<span data-ttu-id="9dcae-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9dcae-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9dcae-163">Optional</span><span class="sxs-lookup"><span data-stu-id="9dcae-163">optional</span></span>  <br/> |<span data-ttu-id="9dcae-164">Ein Wert, der die Form identifiziert, auf der sich der Kommentar befindet.</span><span class="sxs-lookup"><span data-stu-id="9dcae-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="9dcae-165">Wenn keine ShapeID angegeben ist, bezieht sich der Kommentar auf das Zeichenblatt.</span><span class="sxs-lookup"><span data-stu-id="9dcae-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="9dcae-166">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9dcae-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

