---
title: Comments_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: b2d40b1c8368945cfa27aad0e1d567beea694c28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359409"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="378f2-102">Comments_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="378f2-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="378f2-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="378f2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="378f2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="378f2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="378f2-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="378f2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="378f2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="378f2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="378f2-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="378f2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="378f2-108">Keine</span><span class="sxs-lookup"><span data-stu-id="378f2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="378f2-109">Definition</span><span class="sxs-lookup"><span data-stu-id="378f2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="378f2-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="378f2-110">Elements and attributes</span></span>

<span data-ttu-id="378f2-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="378f2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="378f2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="378f2-112">Child elements</span></span>

|<span data-ttu-id="378f2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="378f2-113">**Element**</span></span>|<span data-ttu-id="378f2-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="378f2-114">**Type**</span></span>|<span data-ttu-id="378f2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="378f2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="378f2-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="378f2-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="378f2-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="378f2-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="378f2-118">Kommentarlist</span><span class="sxs-lookup"><span data-stu-id="378f2-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="378f2-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="378f2-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="378f2-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="378f2-120">Attributes</span></span>

|<span data-ttu-id="378f2-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="378f2-121">**Attribute**</span></span>|<span data-ttu-id="378f2-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="378f2-122">**Type**</span></span>|<span data-ttu-id="378f2-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="378f2-123">**Required**</span></span>|<span data-ttu-id="378f2-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="378f2-124">**Description**</span></span>|<span data-ttu-id="378f2-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="378f2-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="378f2-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="378f2-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="378f2-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="378f2-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="378f2-128">Optional</span><span class="sxs-lookup"><span data-stu-id="378f2-128">optional</span></span>  <br/> ||<span data-ttu-id="378f2-129">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="378f2-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

