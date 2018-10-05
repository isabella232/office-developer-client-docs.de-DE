---
title: Comments_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: b2d40b1c8368945cfa27aad0e1d567beea694c28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393474"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="6bbae-102">Comments_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6bbae-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6bbae-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6bbae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bbae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6bbae-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6bbae-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6bbae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6bbae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6bbae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6bbae-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6bbae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6bbae-108">Keine</span><span class="sxs-lookup"><span data-stu-id="6bbae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6bbae-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6bbae-109">Definition</span></span>

```XML
          <xs:complexType name="Comments_Type">
          
          <xs:sequence>
    <xs:element name="AuthorList"  type="AuthorList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CommentList"  type="CommentList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ShowCommentTags"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6bbae-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6bbae-110">Elements and attributes</span></span>

<span data-ttu-id="6bbae-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6bbae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6bbae-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6bbae-112">Child elements</span></span>

|<span data-ttu-id="6bbae-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bbae-113">**Element**</span></span>|<span data-ttu-id="6bbae-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6bbae-114">**Type**</span></span>|<span data-ttu-id="6bbae-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bbae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6bbae-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="6bbae-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6bbae-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="6bbae-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6bbae-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="6bbae-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6bbae-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="6bbae-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6bbae-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="6bbae-120">Attributes</span></span>

|<span data-ttu-id="6bbae-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6bbae-121">**Attribute**</span></span>|<span data-ttu-id="6bbae-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6bbae-122">**Type**</span></span>|<span data-ttu-id="6bbae-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6bbae-123">**Required**</span></span>|<span data-ttu-id="6bbae-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bbae-124">**Description**</span></span>|<span data-ttu-id="6bbae-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6bbae-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6bbae-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="6bbae-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="6bbae-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="6bbae-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6bbae-128">Optional</span><span class="sxs-lookup"><span data-stu-id="6bbae-128">optional</span></span>  <br/> ||<span data-ttu-id="6bbae-129">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="6bbae-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

