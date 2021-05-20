---
title: Comments-Element (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Gibt Eigenschaften an, die zum Identifizieren der Autoren und Kommentare in einer Zeichnung verwendet werden.
ms.openlocfilehash: 93e75e47a203ee13385085c4b5e261fd3a724d4f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539220"
---
# <a name="comments-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="cc0de-103">Comments-Element (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cc0de-103">Comments element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="cc0de-104">Gibt Eigenschaften an, die zum Identifizieren der Autoren und Kommentare in einer Zeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc0de-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc0de-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cc0de-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc0de-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="cc0de-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc0de-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="cc0de-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cc0de-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc0de-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cc0de-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cc0de-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc0de-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cc0de-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cc0de-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="cc0de-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cc0de-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="cc0de-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc0de-113">Definition</span><span class="sxs-lookup"><span data-stu-id="cc0de-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc0de-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cc0de-114">Elements and attributes</span></span>

<span data-ttu-id="cc0de-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cc0de-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc0de-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc0de-116">Parent elements</span></span>

<span data-ttu-id="cc0de-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc0de-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc0de-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc0de-118">Child elements</span></span>

|<span data-ttu-id="cc0de-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc0de-119">**Element**</span></span>|<span data-ttu-id="cc0de-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cc0de-120">**Type**</span></span>|<span data-ttu-id="cc0de-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc0de-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc0de-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="cc0de-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc0de-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="cc0de-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc0de-124">Gibt die Autoren in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="cc0de-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="cc0de-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="cc0de-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc0de-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="cc0de-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc0de-127">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="cc0de-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cc0de-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc0de-128">Attributes</span></span>

<span data-ttu-id="cc0de-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc0de-129">None.</span></span>
  

