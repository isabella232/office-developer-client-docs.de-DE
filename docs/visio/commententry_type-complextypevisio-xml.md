---
title: CommentEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384794"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="fde71-102">CommentEntry_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="fde71-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fde71-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="fde71-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fde71-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fde71-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fde71-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fde71-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fde71-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fde71-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fde71-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="fde71-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fde71-108">XSD: String</span><span class="sxs-lookup"><span data-stu-id="fde71-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fde71-109">Definition</span><span class="sxs-lookup"><span data-stu-id="fde71-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fde71-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fde71-110">Elements and attributes</span></span>

<span data-ttu-id="fde71-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="fde71-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fde71-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fde71-112">Child elements</span></span>

<span data-ttu-id="fde71-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="fde71-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fde71-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="fde71-114">Attributes</span></span>

|<span data-ttu-id="fde71-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fde71-115">**Attribute**</span></span>|<span data-ttu-id="fde71-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fde71-116">**Type**</span></span>|<span data-ttu-id="fde71-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="fde71-117">**Required**</span></span>|<span data-ttu-id="fde71-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fde71-118">**Description**</span></span>|<span data-ttu-id="fde71-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="fde71-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fde71-120">AutorID</span><span class="sxs-lookup"><span data-stu-id="fde71-120">AuthorID</span></span>  <br/> |<span data-ttu-id="fde71-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fde71-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fde71-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde71-122">required</span></span>  <br/> ||<span data-ttu-id="fde71-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fde71-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fde71-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="fde71-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="fde71-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fde71-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fde71-126">Optional</span><span class="sxs-lookup"><span data-stu-id="fde71-126">optional</span></span>  <br/> ||<span data-ttu-id="fde71-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fde71-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fde71-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="fde71-128">CommentID</span></span>  <br/> |<span data-ttu-id="fde71-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fde71-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fde71-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde71-130">required</span></span>  <br/> ||<span data-ttu-id="fde71-131">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fde71-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fde71-132">Datum</span><span class="sxs-lookup"><span data-stu-id="fde71-132">Date</span></span>  <br/> |<span data-ttu-id="fde71-133">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="fde71-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="fde71-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde71-134">required</span></span>  <br/> ||<span data-ttu-id="fde71-135">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="fde71-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="fde71-136">Fertig</span><span class="sxs-lookup"><span data-stu-id="fde71-136">Done</span></span>  <br/> |<span data-ttu-id="fde71-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="fde71-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fde71-138">Optional</span><span class="sxs-lookup"><span data-stu-id="fde71-138">optional</span></span>  <br/> ||<span data-ttu-id="fde71-139">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="fde71-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fde71-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="fde71-140">EditDate</span></span>  <br/> |<span data-ttu-id="fde71-141">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="fde71-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="fde71-142">Optional</span><span class="sxs-lookup"><span data-stu-id="fde71-142">optional</span></span>  <br/> ||<span data-ttu-id="fde71-143">Werte des Typs xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="fde71-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="fde71-144">PageID</span><span class="sxs-lookup"><span data-stu-id="fde71-144">PageID</span></span>  <br/> |<span data-ttu-id="fde71-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fde71-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fde71-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde71-146">required</span></span>  <br/> ||<span data-ttu-id="fde71-147">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fde71-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fde71-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="fde71-148">ShapeID</span></span>  <br/> |<span data-ttu-id="fde71-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fde71-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fde71-150">Optional</span><span class="sxs-lookup"><span data-stu-id="fde71-150">optional</span></span>  <br/> ||<span data-ttu-id="fde71-151">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fde71-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

