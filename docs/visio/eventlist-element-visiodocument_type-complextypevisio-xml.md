---
title: EventList-Element (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Enthält ein EventItem-Element für jedes Ereignis, auf das ein Objekt reagieren soll.
ms.openlocfilehash: 5331f1b4a510b05b862f8c7c6306c89c6be4d9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351051"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="1d8f2-103">EventList-Element (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1d8f2-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1d8f2-104">Enthält ein **EventItem** -Element für jedes Ereignis, auf das ein Objekt reagieren soll.</span><span class="sxs-lookup"><span data-stu-id="1d8f2-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1d8f2-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1d8f2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d8f2-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1d8f2-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="1d8f2-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1d8f2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1d8f2-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1d8f2-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1d8f2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1d8f2-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1d8f2-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="1d8f2-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d8f2-113">Definition</span><span class="sxs-lookup"><span data-stu-id="1d8f2-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1d8f2-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1d8f2-114">Elements and attributes</span></span>

<span data-ttu-id="1d8f2-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1d8f2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1d8f2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d8f2-116">Parent elements</span></span>

|<span data-ttu-id="1d8f2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-117">**Element**</span></span>|<span data-ttu-id="1d8f2-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-118">**Type**</span></span>|<span data-ttu-id="1d8f2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d8f2-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="1d8f2-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="1d8f2-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="1d8f2-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1d8f2-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="1d8f2-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d8f2-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d8f2-123">Child elements</span></span>

|<span data-ttu-id="1d8f2-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-124">**Element**</span></span>|<span data-ttu-id="1d8f2-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-125">**Type**</span></span>|<span data-ttu-id="1d8f2-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d8f2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d8f2-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="1d8f2-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d8f2-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="1d8f2-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1d8f2-129">Kapselt einen Ereigniscode.</span><span class="sxs-lookup"><span data-stu-id="1d8f2-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1d8f2-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d8f2-130">Attributes</span></span>

<span data-ttu-id="1d8f2-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d8f2-131">None.</span></span>
  

