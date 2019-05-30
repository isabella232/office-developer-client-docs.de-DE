---
title: Comments_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: cce19353343190225efedec7f0a5c7bc0f026705
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542016"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="b49f5-102">Comments_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b49f5-102">Comments_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b49f5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b49f5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b49f5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b49f5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b49f5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b49f5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b49f5-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b49f5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b49f5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b49f5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b49f5-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b49f5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b49f5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b49f5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b49f5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b49f5-110">Elements and attributes</span></span>

<span data-ttu-id="b49f5-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b49f5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b49f5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b49f5-112">Child elements</span></span>

|<span data-ttu-id="b49f5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b49f5-113">**Element**</span></span>|<span data-ttu-id="b49f5-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b49f5-114">**Type**</span></span>|<span data-ttu-id="b49f5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b49f5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b49f5-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="b49f5-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b49f5-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="b49f5-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b49f5-118">Kommentarliste</span><span class="sxs-lookup"><span data-stu-id="b49f5-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b49f5-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="b49f5-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b49f5-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="b49f5-120">Attributes</span></span>

|<span data-ttu-id="b49f5-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b49f5-121">**Attribute**</span></span>|<span data-ttu-id="b49f5-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b49f5-122">**Type**</span></span>|<span data-ttu-id="b49f5-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b49f5-123">**Required**</span></span>|<span data-ttu-id="b49f5-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b49f5-124">**Description**</span></span>|<span data-ttu-id="b49f5-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b49f5-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b49f5-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="b49f5-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="b49f5-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="b49f5-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b49f5-128">Optional</span><span class="sxs-lookup"><span data-stu-id="b49f5-128">optional</span></span>  <br/> ||<span data-ttu-id="b49f5-129">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="b49f5-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

