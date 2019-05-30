---
title: EventList-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Enthält ein EventItem-Element für jedes Ereignis, auf das ein Objekt reagieren soll.
ms.openlocfilehash: 7b1406f56dddd8507e330aa93d5cfe9f390caf21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541799"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="b5f3f-103">EventList-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b5f3f-103">EventList element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b5f3f-104">Enthält ein **EventItem** -Element für jedes Ereignis, auf das ein Objekt reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="b5f3f-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b5f3f-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5f3f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5f3f-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5f3f-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="b5f3f-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5f3f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5f3f-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5f3f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b5f3f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5f3f-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5f3f-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="b5f3f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5f3f-113">Definition</span><span class="sxs-lookup"><span data-stu-id="b5f3f-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5f3f-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b5f3f-114">Elements and attributes</span></span>

<span data-ttu-id="b5f3f-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b5f3f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5f3f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5f3f-116">Parent elements</span></span>

|<span data-ttu-id="b5f3f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-117">**Element**</span></span>|<span data-ttu-id="b5f3f-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-118">**Type**</span></span>|<span data-ttu-id="b5f3f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5f3f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="b5f3f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="b5f3f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="b5f3f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5f3f-122">Das Stammelement eines Microsoft Visio Dokuments.</span><span class="sxs-lookup"><span data-stu-id="b5f3f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5f3f-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5f3f-123">Child elements</span></span>

|<span data-ttu-id="b5f3f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-124">**Element**</span></span>|<span data-ttu-id="b5f3f-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-125">**Type**</span></span>|<span data-ttu-id="b5f3f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5f3f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5f3f-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="b5f3f-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5f3f-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="b5f3f-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5f3f-129">Kapselt einen Ereigniscode.</span><span class="sxs-lookup"><span data-stu-id="b5f3f-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b5f3f-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5f3f-130">Attributes</span></span>

<span data-ttu-id="b5f3f-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5f3f-131">None.</span></span>
  

