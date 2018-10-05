---
title: Comments-Element (Comments_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Gibt Eigenschaften verwendet, um die Autoren und Kommentare in einer Zeichnung zu identifizieren.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389645"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="20b62-103">Comments-Element (Comments_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="20b62-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="20b62-104">Gibt Eigenschaften verwendet, um die Autoren und Kommentare in einer Zeichnung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="20b62-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20b62-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="20b62-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20b62-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="20b62-106">**Element type**</span></span> <br/> |[<span data-ttu-id="20b62-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="20b62-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="20b62-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20b62-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="20b62-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="20b62-109">**Schema file**</span></span> <br/> |<span data-ttu-id="20b62-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="20b62-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="20b62-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="20b62-111">**Document parts**</span></span> <br/> |<span data-ttu-id="20b62-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="20b62-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20b62-113">Definition</span><span class="sxs-lookup"><span data-stu-id="20b62-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="20b62-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="20b62-114">Elements and attributes</span></span>

<span data-ttu-id="20b62-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="20b62-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="20b62-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20b62-116">Parent elements</span></span>

<span data-ttu-id="20b62-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="20b62-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20b62-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20b62-118">Child elements</span></span>

|<span data-ttu-id="20b62-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="20b62-119">**Element**</span></span>|<span data-ttu-id="20b62-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="20b62-120">**Type**</span></span>|<span data-ttu-id="20b62-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20b62-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20b62-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="20b62-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20b62-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="20b62-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20b62-124">Gibt die Autoren in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="20b62-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="20b62-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="20b62-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20b62-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="20b62-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20b62-127">Gibt die Kommentare in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="20b62-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="20b62-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="20b62-128">Attributes</span></span>

<span data-ttu-id="20b62-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="20b62-129">None.</span></span>
  

