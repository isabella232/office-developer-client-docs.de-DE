---
title: Commentlist-Element (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Gibt die Kommentare in einer Zeichnung an.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359430"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="c07ea-103">Commentlist-Element (Comments_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c07ea-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c07ea-104">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c07ea-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c07ea-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c07ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c07ea-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c07ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c07ea-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="c07ea-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c07ea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c07ea-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c07ea-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c07ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c07ea-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c07ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c07ea-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="c07ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c07ea-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="c07ea-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c07ea-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c07ea-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c07ea-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c07ea-114">Elements and attributes</span></span>

<span data-ttu-id="c07ea-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c07ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c07ea-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c07ea-116">Parent elements</span></span>

|<span data-ttu-id="c07ea-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c07ea-117">**Element**</span></span>|<span data-ttu-id="c07ea-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c07ea-118">**Type**</span></span>|<span data-ttu-id="c07ea-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c07ea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c07ea-120">Comments</span><span class="sxs-lookup"><span data-stu-id="c07ea-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c07ea-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="c07ea-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c07ea-122">Gibt die Eigenschaften an, die zum Identifizieren der Autoren und Kommentare in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c07ea-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c07ea-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c07ea-123">Child elements</span></span>

|<span data-ttu-id="c07ea-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c07ea-124">**Element**</span></span>|<span data-ttu-id="c07ea-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c07ea-125">**Type**</span></span>|<span data-ttu-id="c07ea-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c07ea-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c07ea-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="c07ea-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c07ea-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c07ea-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c07ea-129">Gibt die Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c07ea-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c07ea-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="c07ea-130">Attributes</span></span>

<span data-ttu-id="c07ea-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="c07ea-131">None.</span></span>
  

