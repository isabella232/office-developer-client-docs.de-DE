---
title: Commentlist-Element (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Gibt die Kommentare in einer Zeichnung an.
ms.openlocfilehash: fbbc7ea668686a8f075f3f11843b2d828c257363
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539248"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="61579-103">Commentlist-Element (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="61579-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="61579-104">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="61579-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61579-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="61579-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61579-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="61579-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61579-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="61579-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61579-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61579-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61579-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="61579-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61579-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="61579-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61579-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="61579-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61579-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="61579-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61579-113">Definition</span><span class="sxs-lookup"><span data-stu-id="61579-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61579-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="61579-114">Elements and attributes</span></span>

<span data-ttu-id="61579-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="61579-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61579-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61579-116">Parent elements</span></span>

|<span data-ttu-id="61579-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="61579-117">**Element**</span></span>|<span data-ttu-id="61579-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="61579-118">**Type**</span></span>|<span data-ttu-id="61579-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61579-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61579-120">Kommentare</span><span class="sxs-lookup"><span data-stu-id="61579-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61579-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="61579-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61579-122">Gibt Eigenschaften an, die zum Identifizieren der Autoren und Kommentare in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61579-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61579-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61579-123">Child elements</span></span>

|<span data-ttu-id="61579-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="61579-124">**Element**</span></span>|<span data-ttu-id="61579-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="61579-125">**Type**</span></span>|<span data-ttu-id="61579-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61579-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61579-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="61579-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61579-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="61579-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61579-129">Gibt Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61579-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="61579-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="61579-130">Attributes</span></span>

<span data-ttu-id="61579-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="61579-131">None.</span></span>
  

