---
title: Shapes-Element (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Enthält eine Auflistung von Shape-Elementen.
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542121"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="121b4-103">Shapes-Element (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="121b4-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="121b4-104">Enthält eine Auflistung von Shape-Elementen.</span><span class="sxs-lookup"><span data-stu-id="121b4-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="121b4-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="121b4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="121b4-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="121b4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="121b4-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="121b4-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="121b4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="121b4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="121b4-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="121b4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="121b4-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="121b4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="121b4-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="121b4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="121b4-112">Seite #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="121b4-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="121b4-113">Definition</span><span class="sxs-lookup"><span data-stu-id="121b4-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="121b4-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="121b4-114">Elements and attributes</span></span>

<span data-ttu-id="121b4-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="121b4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="121b4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="121b4-116">Parent elements</span></span>

|<span data-ttu-id="121b4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="121b4-117">**Element**</span></span>|<span data-ttu-id="121b4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="121b4-118">**Type**</span></span>|<span data-ttu-id="121b4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="121b4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="121b4-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="121b4-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="121b4-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="121b4-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="121b4-122">Gibt Informationen zu den Shapes in einem Master-Shape in einer webzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="121b4-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="121b4-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="121b4-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="121b4-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="121b4-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="121b4-125">Gibt Informationen zu den Shapes in einem Master-Shape in einer webzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="121b4-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="121b4-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="121b4-126">Child elements</span></span>

|<span data-ttu-id="121b4-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="121b4-127">**Element**</span></span>|<span data-ttu-id="121b4-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="121b4-128">**Type**</span></span>|<span data-ttu-id="121b4-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="121b4-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="121b4-130">Shape</span><span class="sxs-lookup"><span data-stu-id="121b4-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="121b4-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="121b4-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="121b4-132">Enthält Elemente, die eine Form in einem **Master**-Shape, einem **Seiten**-oder Gruppen-Shape-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="121b4-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="121b4-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="121b4-133">Attributes</span></span>

<span data-ttu-id="121b4-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="121b4-134">None.</span></span>
  

