---
title: CommentList-Element (Comments_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Gibt die Kommentare in einer Zeichnung.
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796671"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="6d969-103">CommentList-Element (Comments_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="6d969-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6d969-104">Gibt die Kommentare in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="6d969-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d969-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6d969-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d969-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6d969-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6d969-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="6d969-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6d969-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d969-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6d969-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6d969-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6d969-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6d969-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6d969-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="6d969-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6d969-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="6d969-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d969-113">Definition</span><span class="sxs-lookup"><span data-stu-id="6d969-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d969-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6d969-114">Elements and attributes</span></span>

<span data-ttu-id="6d969-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="6d969-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6d969-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d969-116">Parent elements</span></span>

|<span data-ttu-id="6d969-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d969-117">**Element**</span></span>|<span data-ttu-id="6d969-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6d969-118">**Type**</span></span>|<span data-ttu-id="6d969-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d969-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d969-120">Comments</span><span class="sxs-lookup"><span data-stu-id="6d969-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6d969-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="6d969-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6d969-122">Gibt Eigenschaften verwendet, um die Autoren und Kommentare in einer Zeichnung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6d969-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6d969-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d969-123">Child elements</span></span>

|<span data-ttu-id="6d969-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d969-124">**Element**</span></span>|<span data-ttu-id="6d969-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6d969-125">**Type**</span></span>|<span data-ttu-id="6d969-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d969-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d969-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="6d969-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6d969-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="6d969-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6d969-129">Gibt Eigenschaften verwendet, um einen Kommentar in einer Zeichnung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6d969-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6d969-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d969-130">Attributes</span></span>

<span data-ttu-id="6d969-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d969-131">None.</span></span>
  

