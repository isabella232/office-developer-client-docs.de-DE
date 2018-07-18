---
title: WeatherType ComplexType (Outlook Wetter Speicherort-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Definiert die Parameter Wetter Bedingungen von einem Speicherort an.
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796181"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="b694b-103">WeatherType ComplexType (Outlook Wetter Speicherort-Schema)</span><span class="sxs-lookup"><span data-stu-id="b694b-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="b694b-104">Definiert die Parameter Wetter Bedingungen von einem Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="b694b-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="b694b-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b694b-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b694b-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b694b-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="b694b-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b694b-107">**Schema file**</span></span> <br/> |<span data-ttu-id="b694b-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="b694b-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="b694b-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b694b-109">**Extension base**</span></span> <br/> |<span data-ttu-id="b694b-110">Keine</span><span class="sxs-lookup"><span data-stu-id="b694b-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b694b-111">Definition</span><span class="sxs-lookup"><span data-stu-id="b694b-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="b694b-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b694b-112">Elements and attributes</span></span>

<span data-ttu-id="b694b-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b694b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b694b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b694b-114">Child elements</span></span>

<span data-ttu-id="b694b-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="b694b-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b694b-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="b694b-116">Attributes</span></span>

|<span data-ttu-id="b694b-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b694b-117">**Attribute**</span></span>|<span data-ttu-id="b694b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b694b-118">**Type**</span></span>|<span data-ttu-id="b694b-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b694b-119">**Required**</span></span>|<span data-ttu-id="b694b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b694b-120">**Description**</span></span>|<span data-ttu-id="b694b-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b694b-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b694b-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="b694b-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="b694b-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="b694b-123">xs:string</span></span>  <br/> |<span data-ttu-id="b694b-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b694b-124">required</span></span>  <br/> |<span data-ttu-id="b694b-125">Gibt einen Code, der den Speicherort zum unterscheiden von mehreren Standorten mit dem gleichen Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b694b-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="b694b-126">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="b694b-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b694b-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="b694b-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="b694b-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="b694b-128">xs:string</span></span>  <br/> |<span data-ttu-id="b694b-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b694b-129">required</span></span>  <br/> |<span data-ttu-id="b694b-130">Gibt den Namen des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="b694b-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="b694b-131">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="b694b-131">A value of the type xs:string</span></span>  <br/> |
   

