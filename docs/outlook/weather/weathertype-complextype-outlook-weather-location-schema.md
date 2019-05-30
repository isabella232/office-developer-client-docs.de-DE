---
title: weathertype complexType (Outlook-Wetter Standort Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Definiert die Parameter für die Wetterbedingungen eines Standorts.
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542919"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="7443d-103">weathertype complexType (Outlook-Wetter Standort Schema)</span><span class="sxs-lookup"><span data-stu-id="7443d-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="7443d-104">Definiert die Parameter für die Wetterbedingungen eines Standorts.</span><span class="sxs-lookup"><span data-stu-id="7443d-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="7443d-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="7443d-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7443d-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7443d-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="7443d-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7443d-107">**Schema file**</span></span> <br/> |<span data-ttu-id="7443d-108">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="7443d-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="7443d-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="7443d-109">**Extension base**</span></span> <br/> |<span data-ttu-id="7443d-110">Keine</span><span class="sxs-lookup"><span data-stu-id="7443d-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7443d-111">Definition</span><span class="sxs-lookup"><span data-stu-id="7443d-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="7443d-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7443d-112">Elements and attributes</span></span>

<span data-ttu-id="7443d-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7443d-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7443d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7443d-114">Child elements</span></span>

<span data-ttu-id="7443d-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="7443d-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7443d-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="7443d-116">Attributes</span></span>

|<span data-ttu-id="7443d-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7443d-117">**Attribute**</span></span>|<span data-ttu-id="7443d-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7443d-118">**Type**</span></span>|<span data-ttu-id="7443d-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7443d-119">**Required**</span></span>|<span data-ttu-id="7443d-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7443d-120">**Description**</span></span>|<span data-ttu-id="7443d-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7443d-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7443d-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="7443d-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="7443d-123">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7443d-123">xs:string</span></span>  <br/> |<span data-ttu-id="7443d-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7443d-124">required</span></span>  <br/> |<span data-ttu-id="7443d-125">Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Standorte mit dem gleichen Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7443d-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="7443d-126">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="7443d-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7443d-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="7443d-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="7443d-128">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7443d-128">xs:string</span></span>  <br/> |<span data-ttu-id="7443d-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7443d-129">required</span></span>  <br/> |<span data-ttu-id="7443d-130">Gibt den Namen des Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="7443d-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="7443d-131">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="7443d-131">A value of the type xs:string</span></span>  <br/> |
   

