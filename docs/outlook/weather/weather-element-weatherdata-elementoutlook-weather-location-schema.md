---
title: wetterelement (weatherdata element) (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Gibt den Ort an, an dem das Wetter berichtet werden soll.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539012"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="dc51a-103">wetterelement (weatherdata element) (Outlook Weather Location Schema)</span><span class="sxs-lookup"><span data-stu-id="dc51a-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="dc51a-104">Gibt den Ort an, an dem das Wetter berichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc51a-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc51a-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dc51a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc51a-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="dc51a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dc51a-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="dc51a-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="dc51a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dc51a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="dc51a-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="dc51a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dc51a-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="dc51a-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc51a-111">Definition</span><span class="sxs-lookup"><span data-stu-id="dc51a-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc51a-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="dc51a-112">Elements and attributes</span></span>

<span data-ttu-id="dc51a-113">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="dc51a-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dc51a-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc51a-114">Parent elements</span></span>

|<span data-ttu-id="dc51a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc51a-115">**Element**</span></span>|<span data-ttu-id="dc51a-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="dc51a-116">**Type**</span></span>|<span data-ttu-id="dc51a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc51a-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dc51a-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="dc51a-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="dc51a-119">Definiert das Wetterelement.</span><span class="sxs-lookup"><span data-stu-id="dc51a-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dc51a-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc51a-120">Child elements</span></span>

<span data-ttu-id="dc51a-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc51a-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc51a-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc51a-122">Attributes</span></span>

|<span data-ttu-id="dc51a-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dc51a-123">**Attribute**</span></span>|<span data-ttu-id="dc51a-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="dc51a-124">**Type**</span></span>|<span data-ttu-id="dc51a-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="dc51a-125">**Required**</span></span>|<span data-ttu-id="dc51a-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc51a-126">**Description**</span></span>|<span data-ttu-id="dc51a-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="dc51a-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc51a-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="dc51a-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="dc51a-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="dc51a-129">xs:string</span></span>  <br/> |<span data-ttu-id="dc51a-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc51a-130">required</span></span>  <br/> |<span data-ttu-id="dc51a-131">Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Speicherorte mit demselben Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="dc51a-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="dc51a-132">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="dc51a-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="dc51a-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="dc51a-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="dc51a-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="dc51a-134">xs:string</span></span>  <br/> |<span data-ttu-id="dc51a-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc51a-135">required</span></span>  <br/> |<span data-ttu-id="dc51a-136">Gibt den Namen des Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="dc51a-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="dc51a-137">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="dc51a-137">A value of the type xs:string</span></span>  <br/> |
   

