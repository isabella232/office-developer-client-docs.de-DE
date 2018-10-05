---
title: EventList-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Enthält ein Element EventItem für jedes Ereignis, der ein Objekt Antworten sollen.
ms.openlocfilehash: 5331f1b4a510b05b862f8c7c6306c89c6be4d9f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383975"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="60f7a-103">EventList-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="60f7a-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="60f7a-104">Enthält ein Element **EventItem** für jedes Ereignis, der ein Objekt Antworten sollen.</span><span class="sxs-lookup"><span data-stu-id="60f7a-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="60f7a-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="60f7a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60f7a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="60f7a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="60f7a-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="60f7a-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="60f7a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="60f7a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="60f7a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="60f7a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="60f7a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="60f7a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="60f7a-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="60f7a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="60f7a-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="60f7a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="60f7a-113">Definition</span><span class="sxs-lookup"><span data-stu-id="60f7a-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="60f7a-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="60f7a-114">Elements and attributes</span></span>

<span data-ttu-id="60f7a-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="60f7a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="60f7a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60f7a-116">Parent elements</span></span>

|<span data-ttu-id="60f7a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="60f7a-117">**Element**</span></span>|<span data-ttu-id="60f7a-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="60f7a-118">**Type**</span></span>|<span data-ttu-id="60f7a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60f7a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="60f7a-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="60f7a-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="60f7a-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="60f7a-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="60f7a-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="60f7a-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="60f7a-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60f7a-123">Child elements</span></span>

|<span data-ttu-id="60f7a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="60f7a-124">**Element**</span></span>|<span data-ttu-id="60f7a-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="60f7a-125">**Type**</span></span>|<span data-ttu-id="60f7a-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60f7a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="60f7a-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="60f7a-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="60f7a-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="60f7a-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="60f7a-129">Einen Ereigniscode kapselt.</span><span class="sxs-lookup"><span data-stu-id="60f7a-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="60f7a-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="60f7a-130">Attributes</span></span>

<span data-ttu-id="60f7a-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="60f7a-131">None.</span></span>
  

