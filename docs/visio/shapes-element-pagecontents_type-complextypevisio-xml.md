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
# <a name="shapes-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="94039-103">Shapes-Element (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="94039-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="94039-104">Enthält eine Auflistung von Shape-Elementen.</span><span class="sxs-lookup"><span data-stu-id="94039-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94039-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="94039-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94039-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="94039-106">**Element type**</span></span> <br/> |[<span data-ttu-id="94039-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="94039-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="94039-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="94039-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="94039-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="94039-109">**Schema file**</span></span> <br/> |<span data-ttu-id="94039-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="94039-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="94039-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="94039-111">**Document parts**</span></span> <br/> |<span data-ttu-id="94039-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="94039-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94039-113">Definition</span><span class="sxs-lookup"><span data-stu-id="94039-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="94039-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="94039-114">Elements and attributes</span></span>

<span data-ttu-id="94039-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="94039-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="94039-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="94039-116">Parent elements</span></span>

|<span data-ttu-id="94039-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="94039-117">**Element**</span></span>|<span data-ttu-id="94039-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="94039-118">**Type**</span></span>|<span data-ttu-id="94039-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94039-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="94039-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="94039-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="94039-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="94039-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94039-122">Gibt Informationen zu den Formen in einem Master in einer Webzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="94039-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="94039-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="94039-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="94039-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="94039-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94039-125">Gibt Informationen zu den Formen in einem Master in einer Webzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="94039-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94039-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="94039-126">Child elements</span></span>

|<span data-ttu-id="94039-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="94039-127">**Element**</span></span>|<span data-ttu-id="94039-128">**Typ**</span><span class="sxs-lookup"><span data-stu-id="94039-128">**Type**</span></span>|<span data-ttu-id="94039-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94039-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="94039-130">Shape</span><span class="sxs-lookup"><span data-stu-id="94039-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="94039-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="94039-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94039-132">Enthält Elemente, die ein Shape in einem **Master-,** **Page-** oder Gruppenformelement definieren.</span><span class="sxs-lookup"><span data-stu-id="94039-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="94039-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="94039-133">Attributes</span></span>

<span data-ttu-id="94039-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="94039-134">None.</span></span>
  

