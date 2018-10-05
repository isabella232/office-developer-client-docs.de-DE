---
title: CommentList-Element (Comments_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Gibt die Kommentare in einer Zeichnung.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395168"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="2ff11-103">CommentList-Element (Comments_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="2ff11-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2ff11-104">Gibt die Kommentare in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="2ff11-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ff11-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2ff11-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ff11-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="2ff11-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2ff11-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="2ff11-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2ff11-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2ff11-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2ff11-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2ff11-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2ff11-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2ff11-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2ff11-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="2ff11-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2ff11-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="2ff11-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2ff11-113">Definition</span><span class="sxs-lookup"><span data-stu-id="2ff11-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2ff11-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2ff11-114">Elements and attributes</span></span>

<span data-ttu-id="2ff11-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="2ff11-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2ff11-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ff11-116">Parent elements</span></span>

|<span data-ttu-id="2ff11-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ff11-117">**Element**</span></span>|<span data-ttu-id="2ff11-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2ff11-118">**Type**</span></span>|<span data-ttu-id="2ff11-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ff11-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2ff11-120">Comments</span><span class="sxs-lookup"><span data-stu-id="2ff11-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2ff11-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="2ff11-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2ff11-122">Gibt Eigenschaften verwendet, um die Autoren und Kommentare in einer Zeichnung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2ff11-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2ff11-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ff11-123">Child elements</span></span>

|<span data-ttu-id="2ff11-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ff11-124">**Element**</span></span>|<span data-ttu-id="2ff11-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2ff11-125">**Type**</span></span>|<span data-ttu-id="2ff11-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ff11-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2ff11-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="2ff11-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2ff11-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2ff11-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2ff11-129">Gibt Eigenschaften verwendet, um einen Kommentar in einer Zeichnung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2ff11-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2ff11-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="2ff11-130">Attributes</span></span>

<span data-ttu-id="2ff11-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ff11-131">None.</span></span>
  

