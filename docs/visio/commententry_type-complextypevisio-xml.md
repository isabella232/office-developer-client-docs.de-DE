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
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="ec86e-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ec86e-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ec86e-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ec86e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec86e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ec86e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec86e-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ec86e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec86e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ec86e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec86e-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ec86e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec86e-108">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ec86e-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec86e-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ec86e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec86e-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ec86e-110">Elements and attributes</span></span>

<span data-ttu-id="ec86e-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ec86e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec86e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec86e-112">Child elements</span></span>

<span data-ttu-id="ec86e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec86e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec86e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec86e-114">Attributes</span></span>

|<span data-ttu-id="ec86e-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ec86e-115">**Attribute**</span></span>|<span data-ttu-id="ec86e-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ec86e-116">**Type**</span></span>|<span data-ttu-id="ec86e-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ec86e-117">**Required**</span></span>|<span data-ttu-id="ec86e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec86e-118">**Description**</span></span>|<span data-ttu-id="ec86e-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ec86e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec86e-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="ec86e-120">AuthorID</span></span>  <br/> |<span data-ttu-id="ec86e-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec86e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec86e-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec86e-122">required</span></span>  <br/> ||<span data-ttu-id="ec86e-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec86e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-124">Autocommenttype</span><span class="sxs-lookup"><span data-stu-id="ec86e-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="ec86e-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec86e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec86e-126">Optional</span><span class="sxs-lookup"><span data-stu-id="ec86e-126">optional</span></span>  <br/> ||<span data-ttu-id="ec86e-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec86e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-128">Kommentar-Nr</span><span class="sxs-lookup"><span data-stu-id="ec86e-128">CommentID</span></span>  <br/> |<span data-ttu-id="ec86e-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec86e-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec86e-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec86e-130">required</span></span>  <br/> ||<span data-ttu-id="ec86e-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec86e-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-132">Datum</span><span class="sxs-lookup"><span data-stu-id="ec86e-132">Date</span></span>  <br/> |<span data-ttu-id="ec86e-133">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="ec86e-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="ec86e-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec86e-134">required</span></span>  <br/> ||<span data-ttu-id="ec86e-135">Werte des Typs XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="ec86e-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-136">Fertig</span><span class="sxs-lookup"><span data-stu-id="ec86e-136">Done</span></span>  <br/> |<span data-ttu-id="ec86e-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec86e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec86e-138">Optional</span><span class="sxs-lookup"><span data-stu-id="ec86e-138">optional</span></span>  <br/> ||<span data-ttu-id="ec86e-139">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec86e-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="ec86e-140">EditDate</span></span>  <br/> |<span data-ttu-id="ec86e-141">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="ec86e-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="ec86e-142">Optional</span><span class="sxs-lookup"><span data-stu-id="ec86e-142">optional</span></span>  <br/> ||<span data-ttu-id="ec86e-143">Werte des Typs XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="ec86e-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-144">PageID</span><span class="sxs-lookup"><span data-stu-id="ec86e-144">PageID</span></span>  <br/> |<span data-ttu-id="ec86e-145">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec86e-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec86e-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec86e-146">required</span></span>  <br/> ||<span data-ttu-id="ec86e-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec86e-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec86e-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="ec86e-148">ShapeID</span></span>  <br/> |<span data-ttu-id="ec86e-149">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec86e-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec86e-150">Optional</span><span class="sxs-lookup"><span data-stu-id="ec86e-150">optional</span></span>  <br/> ||<span data-ttu-id="ec86e-151">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ec86e-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

