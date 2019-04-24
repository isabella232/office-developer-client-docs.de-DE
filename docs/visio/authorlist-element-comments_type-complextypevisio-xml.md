---
title: AuthorList-Element (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Gibt die Autoren von Kommentaren in einer Zeichnung an.
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338416"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="c1e89-103">AuthorList-Element (Comments_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c1e89-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c1e89-104">Gibt die Autoren von Kommentaren in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c1e89-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1e89-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c1e89-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1e89-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c1e89-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1e89-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="c1e89-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1e89-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1e89-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1e89-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c1e89-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1e89-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c1e89-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1e89-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="c1e89-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1e89-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="c1e89-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1e89-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c1e89-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1e89-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c1e89-114">Elements and attributes</span></span>

<span data-ttu-id="c1e89-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c1e89-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1e89-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1e89-116">Parent elements</span></span>

|<span data-ttu-id="c1e89-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1e89-117">**Element**</span></span>|<span data-ttu-id="c1e89-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c1e89-118">**Type**</span></span>|<span data-ttu-id="c1e89-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1e89-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1e89-120">Comments</span><span class="sxs-lookup"><span data-stu-id="c1e89-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1e89-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="c1e89-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1e89-122">Gibt die Kommentare in einer Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="c1e89-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1e89-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1e89-123">Child elements</span></span>

|<span data-ttu-id="c1e89-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1e89-124">**Element**</span></span>|<span data-ttu-id="c1e89-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c1e89-125">**Type**</span></span>|<span data-ttu-id="c1e89-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1e89-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1e89-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="c1e89-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1e89-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c1e89-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1e89-129">Gibt die Eigenschaften an, die den Autor eines Kommentars in einer Zeichnung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c1e89-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1e89-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1e89-130">Attributes</span></span>

<span data-ttu-id="c1e89-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1e89-131">None.</span></span>
  

