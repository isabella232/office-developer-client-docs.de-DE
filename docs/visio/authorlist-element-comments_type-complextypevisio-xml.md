---
title: AuthorList-Element (Comments_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Gibt die Autoren von Kommentaren in einer Zeichnung.
ms.openlocfilehash: 0f31e11e52809df60b41cb67b868b15435e0eb47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796438"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="192ba-103">AuthorList-Element (Comments_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="192ba-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="192ba-104">Gibt die Autoren von Kommentaren in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="192ba-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="192ba-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="192ba-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="192ba-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="192ba-106">**Element type**</span></span> <br/> |[<span data-ttu-id="192ba-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="192ba-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="192ba-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="192ba-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="192ba-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="192ba-109">**Schema file**</span></span> <br/> |<span data-ttu-id="192ba-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="192ba-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="192ba-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="192ba-111">**Document parts**</span></span> <br/> |<span data-ttu-id="192ba-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="192ba-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="192ba-113">Definition</span><span class="sxs-lookup"><span data-stu-id="192ba-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="192ba-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="192ba-114">Elements and attributes</span></span>

<span data-ttu-id="192ba-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="192ba-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="192ba-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="192ba-116">Parent elements</span></span>

|<span data-ttu-id="192ba-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="192ba-117">**Element**</span></span>|<span data-ttu-id="192ba-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="192ba-118">**Type**</span></span>|<span data-ttu-id="192ba-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="192ba-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="192ba-120">Comments</span><span class="sxs-lookup"><span data-stu-id="192ba-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192ba-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="192ba-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192ba-122">Gibt die Kommentare in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="192ba-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="192ba-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="192ba-123">Child elements</span></span>

|<span data-ttu-id="192ba-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="192ba-124">**Element**</span></span>|<span data-ttu-id="192ba-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="192ba-125">**Type**</span></span>|<span data-ttu-id="192ba-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="192ba-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="192ba-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="192ba-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192ba-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="192ba-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192ba-129">Gibt die Eigenschaften, die den Autor eines Kommentars in einer Zeichnung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="192ba-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="192ba-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="192ba-130">Attributes</span></span>

<span data-ttu-id="192ba-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="192ba-131">None.</span></span>
  

