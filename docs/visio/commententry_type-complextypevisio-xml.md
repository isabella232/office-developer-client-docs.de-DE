---
title: CommentEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334944"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="6162a-102">CommentEntry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6162a-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6162a-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6162a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6162a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6162a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6162a-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6162a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6162a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6162a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6162a-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6162a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6162a-108">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6162a-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6162a-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6162a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6162a-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6162a-110">Elements and attributes</span></span>

<span data-ttu-id="6162a-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6162a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6162a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6162a-112">Child elements</span></span>

<span data-ttu-id="6162a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="6162a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6162a-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="6162a-114">Attributes</span></span>

|<span data-ttu-id="6162a-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6162a-115">**Attribute**</span></span>|<span data-ttu-id="6162a-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6162a-116">**Type**</span></span>|<span data-ttu-id="6162a-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6162a-117">**Required**</span></span>|<span data-ttu-id="6162a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6162a-118">**Description**</span></span>|<span data-ttu-id="6162a-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6162a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6162a-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="6162a-120">AuthorID</span></span>  <br/> |<span data-ttu-id="6162a-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6162a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6162a-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6162a-122">required</span></span>  <br/> ||<span data-ttu-id="6162a-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6162a-124">AutoCommenttype</span><span class="sxs-lookup"><span data-stu-id="6162a-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="6162a-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6162a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6162a-126">Optional</span><span class="sxs-lookup"><span data-stu-id="6162a-126">optional</span></span>  <br/> ||<span data-ttu-id="6162a-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6162a-128">Kommentar-Nr.</span><span class="sxs-lookup"><span data-stu-id="6162a-128">CommentID</span></span>  <br/> |<span data-ttu-id="6162a-129">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6162a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6162a-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6162a-130">required</span></span>  <br/> ||<span data-ttu-id="6162a-131">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6162a-132">Datum</span><span class="sxs-lookup"><span data-stu-id="6162a-132">Date</span></span>  <br/> |<span data-ttu-id="6162a-133">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="6162a-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="6162a-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6162a-134">required</span></span>  <br/> ||<span data-ttu-id="6162a-135">Werte des XSD: dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="6162a-136">Fertig</span><span class="sxs-lookup"><span data-stu-id="6162a-136">Done</span></span>  <br/> |<span data-ttu-id="6162a-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="6162a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6162a-138">Optional</span><span class="sxs-lookup"><span data-stu-id="6162a-138">optional</span></span>  <br/> ||<span data-ttu-id="6162a-139">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6162a-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="6162a-140">EditDate</span></span>  <br/> |<span data-ttu-id="6162a-141">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="6162a-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="6162a-142">Optional</span><span class="sxs-lookup"><span data-stu-id="6162a-142">optional</span></span>  <br/> ||<span data-ttu-id="6162a-143">Werte des XSD: dateTime-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="6162a-144">PageID</span><span class="sxs-lookup"><span data-stu-id="6162a-144">PageID</span></span>  <br/> |<span data-ttu-id="6162a-145">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6162a-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6162a-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6162a-146">required</span></span>  <br/> ||<span data-ttu-id="6162a-147">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6162a-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="6162a-148">ShapeID</span></span>  <br/> |<span data-ttu-id="6162a-149">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6162a-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6162a-150">Optional</span><span class="sxs-lookup"><span data-stu-id="6162a-150">optional</span></span>  <br/> ||<span data-ttu-id="6162a-151">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6162a-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

