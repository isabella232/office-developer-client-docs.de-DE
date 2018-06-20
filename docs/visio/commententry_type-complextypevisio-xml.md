---
title: CommentEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796659"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="3fb37-102">CommentEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3fb37-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3fb37-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="3fb37-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fb37-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3fb37-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3fb37-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3fb37-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3fb37-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3fb37-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3fb37-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="3fb37-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3fb37-108">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3fb37-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3fb37-109">Definition</span><span class="sxs-lookup"><span data-stu-id="3fb37-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3fb37-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3fb37-110">Elements and attributes</span></span>

<span data-ttu-id="3fb37-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3fb37-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3fb37-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fb37-112">Child elements</span></span>

<span data-ttu-id="3fb37-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fb37-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fb37-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="3fb37-114">Attributes</span></span>

|<span data-ttu-id="3fb37-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3fb37-115">**Attribute**</span></span>|<span data-ttu-id="3fb37-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3fb37-116">**Type**</span></span>|<span data-ttu-id="3fb37-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3fb37-117">**Required**</span></span>|<span data-ttu-id="3fb37-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fb37-118">**Description**</span></span>|<span data-ttu-id="3fb37-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3fb37-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3fb37-120">AutorID</span><span class="sxs-lookup"><span data-stu-id="3fb37-120">AuthorID</span></span>  <br/> |<span data-ttu-id="3fb37-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fb37-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fb37-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fb37-122">required</span></span>  <br/> ||<span data-ttu-id="3fb37-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fb37-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="3fb37-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="3fb37-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fb37-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fb37-126">Optional</span><span class="sxs-lookup"><span data-stu-id="3fb37-126">optional</span></span>  <br/> ||<span data-ttu-id="3fb37-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fb37-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="3fb37-128">CommentID</span></span>  <br/> |<span data-ttu-id="3fb37-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fb37-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fb37-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fb37-130">required</span></span>  <br/> ||<span data-ttu-id="3fb37-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fb37-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-132">Date</span><span class="sxs-lookup"><span data-stu-id="3fb37-132">Date</span></span>  <br/> |<span data-ttu-id="3fb37-133">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="3fb37-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="3fb37-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fb37-134">required</span></span>  <br/> ||<span data-ttu-id="3fb37-135">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="3fb37-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-136">Fertig</span><span class="sxs-lookup"><span data-stu-id="3fb37-136">Done</span></span>  <br/> |<span data-ttu-id="3fb37-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3fb37-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3fb37-138">Optional</span><span class="sxs-lookup"><span data-stu-id="3fb37-138">optional</span></span>  <br/> ||<span data-ttu-id="3fb37-139">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3fb37-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="3fb37-140">EditDate</span></span>  <br/> |<span data-ttu-id="3fb37-141">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="3fb37-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="3fb37-142">Optional</span><span class="sxs-lookup"><span data-stu-id="3fb37-142">optional</span></span>  <br/> ||<span data-ttu-id="3fb37-143">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="3fb37-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-144">PageID</span><span class="sxs-lookup"><span data-stu-id="3fb37-144">PageID</span></span>  <br/> |<span data-ttu-id="3fb37-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fb37-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fb37-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3fb37-146">required</span></span>  <br/> ||<span data-ttu-id="3fb37-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fb37-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3fb37-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="3fb37-148">ShapeID</span></span>  <br/> |<span data-ttu-id="3fb37-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3fb37-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3fb37-150">Optional</span><span class="sxs-lookup"><span data-stu-id="3fb37-150">optional</span></span>  <br/> ||<span data-ttu-id="3fb37-151">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3fb37-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

