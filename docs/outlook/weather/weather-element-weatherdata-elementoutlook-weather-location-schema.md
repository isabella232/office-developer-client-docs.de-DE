---
title: Wetter-Element (Weatherdata-Element) (Outlook Wetter Speicherort-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Gibt den Speicherort für den Bericht Wetter auf.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398297"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="f2c05-103">Wetter-Element (Weatherdata-Element) (Outlook Wetter Speicherort-Schema)</span><span class="sxs-lookup"><span data-stu-id="f2c05-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="f2c05-104">Gibt den Speicherort für den Bericht Wetter auf.</span><span class="sxs-lookup"><span data-stu-id="f2c05-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2c05-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f2c05-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2c05-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f2c05-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f2c05-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="f2c05-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="f2c05-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f2c05-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="f2c05-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f2c05-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f2c05-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="f2c05-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f2c05-111">Definition</span><span class="sxs-lookup"><span data-stu-id="f2c05-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="f2c05-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f2c05-112">Elements and attributes</span></span>

<span data-ttu-id="f2c05-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f2c05-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f2c05-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2c05-114">Parent elements</span></span>

|<span data-ttu-id="f2c05-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2c05-115">**Element**</span></span>|<span data-ttu-id="f2c05-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f2c05-116">**Type**</span></span>|<span data-ttu-id="f2c05-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2c05-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f2c05-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="f2c05-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="f2c05-119">Definiert das Wetter-Element.</span><span class="sxs-lookup"><span data-stu-id="f2c05-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f2c05-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2c05-120">Child elements</span></span>

<span data-ttu-id="f2c05-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2c05-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2c05-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2c05-122">Attributes</span></span>

|<span data-ttu-id="f2c05-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f2c05-123">**Attribute**</span></span>|<span data-ttu-id="f2c05-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f2c05-124">**Type**</span></span>|<span data-ttu-id="f2c05-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f2c05-125">**Required**</span></span>|<span data-ttu-id="f2c05-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2c05-126">**Description**</span></span>|<span data-ttu-id="f2c05-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f2c05-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f2c05-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="f2c05-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="f2c05-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="f2c05-129">xs:string</span></span>  <br/> |<span data-ttu-id="f2c05-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f2c05-130">required</span></span>  <br/> |<span data-ttu-id="f2c05-131">Gibt einen Code, der den Speicherort zum unterscheiden von mehreren Standorten mit dem gleichen Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2c05-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="f2c05-132">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="f2c05-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f2c05-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="f2c05-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="f2c05-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="f2c05-134">xs:string</span></span>  <br/> |<span data-ttu-id="f2c05-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f2c05-135">required</span></span>  <br/> |<span data-ttu-id="f2c05-136">Gibt den Namen des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f2c05-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="f2c05-137">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="f2c05-137">A value of the type xs:string</span></span>  <br/> |
   

