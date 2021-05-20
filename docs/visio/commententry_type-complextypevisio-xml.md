---
title: CommentEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540126"
---
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="20789-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="20789-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="20789-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="20789-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20789-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20789-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="20789-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="20789-105">**Schema file**</span></span> <br/> |<span data-ttu-id="20789-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="20789-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="20789-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="20789-107">**Extension base**</span></span> <br/> |<span data-ttu-id="20789-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20789-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20789-109">Definition</span><span class="sxs-lookup"><span data-stu-id="20789-109">Definition</span></span>

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="20789-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="20789-110">Elements and attributes</span></span>

<span data-ttu-id="20789-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="20789-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="20789-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20789-112">Child elements</span></span>

<span data-ttu-id="20789-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="20789-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20789-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="20789-114">Attributes</span></span>

|<span data-ttu-id="20789-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="20789-115">**Attribute**</span></span>|<span data-ttu-id="20789-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="20789-116">**Type**</span></span>|<span data-ttu-id="20789-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="20789-117">**Required**</span></span>|<span data-ttu-id="20789-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20789-118">**Description**</span></span>|<span data-ttu-id="20789-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="20789-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20789-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="20789-120">AuthorID</span></span>  <br/> |<span data-ttu-id="20789-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20789-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20789-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="20789-122">required</span></span>  <br/> ||<span data-ttu-id="20789-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20789-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="20789-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="20789-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20789-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20789-126">Optional</span><span class="sxs-lookup"><span data-stu-id="20789-126">optional</span></span>  <br/> ||<span data-ttu-id="20789-127">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20789-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="20789-128">CommentID</span></span>  <br/> |<span data-ttu-id="20789-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20789-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20789-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="20789-130">required</span></span>  <br/> ||<span data-ttu-id="20789-131">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20789-132">Datum</span><span class="sxs-lookup"><span data-stu-id="20789-132">Date</span></span>  <br/> |<span data-ttu-id="20789-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="20789-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="20789-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="20789-134">required</span></span>  <br/> ||<span data-ttu-id="20789-135">Werte des xsd:dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="20789-136">Fertig</span><span class="sxs-lookup"><span data-stu-id="20789-136">Done</span></span>  <br/> |<span data-ttu-id="20789-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="20789-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="20789-138">Optional</span><span class="sxs-lookup"><span data-stu-id="20789-138">optional</span></span>  <br/> ||<span data-ttu-id="20789-139">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="20789-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="20789-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="20789-140">EditDate</span></span>  <br/> |<span data-ttu-id="20789-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="20789-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="20789-142">Optional</span><span class="sxs-lookup"><span data-stu-id="20789-142">optional</span></span>  <br/> ||<span data-ttu-id="20789-143">Werte des xsd:dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="20789-144">PageID</span><span class="sxs-lookup"><span data-stu-id="20789-144">PageID</span></span>  <br/> |<span data-ttu-id="20789-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20789-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20789-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="20789-146">required</span></span>  <br/> ||<span data-ttu-id="20789-147">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20789-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="20789-148">ShapeID</span></span>  <br/> |<span data-ttu-id="20789-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20789-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20789-150">Optional</span><span class="sxs-lookup"><span data-stu-id="20789-150">optional</span></span>  <br/> ||<span data-ttu-id="20789-151">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="20789-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

