---
title: Comments-Element (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Gibt die Eigenschaften an, die zum Identifizieren der Autoren und Kommentare in einer Zeichnung verwendet werden.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359395"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="7c2ea-103">Comments-Element (Comments_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7c2ea-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7c2ea-104">Gibt die Eigenschaften an, die zum Identifizieren der Autoren und Kommentare in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c2ea-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7c2ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c2ea-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7c2ea-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7c2ea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7c2ea-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7c2ea-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7c2ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7c2ea-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7c2ea-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="7c2ea-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c2ea-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7c2ea-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c2ea-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7c2ea-114">Elements and attributes</span></span>

<span data-ttu-id="7c2ea-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7c2ea-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c2ea-116">Parent elements</span></span>

<span data-ttu-id="7c2ea-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c2ea-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c2ea-118">Child elements</span></span>

|<span data-ttu-id="7c2ea-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-119">**Element**</span></span>|<span data-ttu-id="7c2ea-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-120">**Type**</span></span>|<span data-ttu-id="7c2ea-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c2ea-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c2ea-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="7c2ea-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-124">Gibt die Autoren in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="7c2ea-125">Kommentarlist</span><span class="sxs-lookup"><span data-stu-id="7c2ea-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c2ea-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="7c2ea-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c2ea-127">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7c2ea-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="7c2ea-128">Attributes</span></span>

<span data-ttu-id="7c2ea-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c2ea-129">None.</span></span>
  

