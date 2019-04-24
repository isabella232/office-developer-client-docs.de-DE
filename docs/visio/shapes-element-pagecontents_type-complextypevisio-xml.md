---
title: Shapes-Element (PageContents_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Enthält eine Auflistung von Shape-Elementen.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349168"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="f553b-103">Shapes-Element (PageContents_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f553b-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f553b-104">Enthält eine Auflistung von Shape-Elementen.</span><span class="sxs-lookup"><span data-stu-id="f553b-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f553b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f553b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f553b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f553b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f553b-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="f553b-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f553b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f553b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f553b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f553b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f553b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f553b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f553b-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="f553b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f553b-112">Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="f553b-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f553b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="f553b-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f553b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f553b-114">Elements and attributes</span></span>

<span data-ttu-id="f553b-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f553b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f553b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f553b-116">Parent elements</span></span>

|<span data-ttu-id="f553b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f553b-117">**Element**</span></span>|<span data-ttu-id="f553b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f553b-118">**Type**</span></span>|<span data-ttu-id="f553b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f553b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f553b-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="f553b-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="f553b-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="f553b-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f553b-122">Gibt Informationen zu den Shapes in einem Master in einer webzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="f553b-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="f553b-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="f553b-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="f553b-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="f553b-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f553b-125">Gibt Informationen zu den Shapes in einem Master in einer webzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="f553b-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f553b-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f553b-126">Child elements</span></span>

|<span data-ttu-id="f553b-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="f553b-127">**Element**</span></span>|<span data-ttu-id="f553b-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f553b-128">**Type**</span></span>|<span data-ttu-id="f553b-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f553b-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f553b-130">Shape</span><span class="sxs-lookup"><span data-stu-id="f553b-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f553b-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f553b-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f553b-132">Enthält Elemente, die eine Form in einem **Master**-, **Page**-oder Group Shape-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="f553b-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f553b-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="f553b-133">Attributes</span></span>

<span data-ttu-id="f553b-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="f553b-134">None.</span></span>
  

