---
title: weatherdata-Element (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Definiert das Wetterelement.
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538984"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="c0e35-103">weatherdata-Element (Outlook Wetterinformationsschema)</span><span class="sxs-lookup"><span data-stu-id="c0e35-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="c0e35-104">Definiert das Wetterelement.</span><span class="sxs-lookup"><span data-stu-id="c0e35-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0e35-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0e35-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0e35-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c0e35-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="c0e35-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c0e35-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="c0e35-108">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c0e35-108">**Schema file**</span></span> <br/> |<span data-ttu-id="c0e35-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="c0e35-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c0e35-110">Definition</span><span class="sxs-lookup"><span data-stu-id="c0e35-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c0e35-111">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c0e35-111">Elements and attributes</span></span>

<span data-ttu-id="c0e35-112">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c0e35-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c0e35-113">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0e35-113">Parent elements</span></span>

<span data-ttu-id="c0e35-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0e35-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0e35-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0e35-115">Child elements</span></span>

|<span data-ttu-id="c0e35-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0e35-116">**Element**</span></span>|<span data-ttu-id="c0e35-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c0e35-117">**Type**</span></span>|<span data-ttu-id="c0e35-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0e35-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c0e35-119">Wetter</span><span class="sxs-lookup"><span data-stu-id="c0e35-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="c0e35-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="c0e35-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="c0e35-121">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="c0e35-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c0e35-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0e35-122">Attributes</span></span>

<span data-ttu-id="c0e35-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0e35-123">None.</span></span>
  

