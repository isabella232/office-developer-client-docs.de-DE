---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Gibt das Datum nach Jahr, Monat und Tag dargestellt entsprechend den Regionaleinstellungen des Systems kurzes Datumsformat formatiert. Die Werte für Jahr, Monat und Tag entsprechend der gregorianische Kalender.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796812"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="5f65b-104">DATE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5f65b-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5f65b-105">Gibt das Datum, die durch *Year, Month* und *Day* entsprechend den Regionaleinstellungen des Systems kurzes Datumsformat formatiert.</span><span class="sxs-lookup"><span data-stu-id="5f65b-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="5f65b-106">Die Werte für *Jahr*, *Monat* und *Tag* entsprechend der gregorianische Kalender.</span><span class="sxs-lookup"><span data-stu-id="5f65b-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5f65b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f65b-107">Syntax</span></span>

<span data-ttu-id="5f65b-108">Datum (** *Jahr* **, ** *Monat* **, ** *Tag* **)</span><span class="sxs-lookup"><span data-stu-id="5f65b-108">DATE(** *year* **, ** *month* **, ** *day* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f65b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f65b-109">Parameters</span></span>

|<span data-ttu-id="5f65b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5f65b-110">**Name**</span></span>|<span data-ttu-id="5f65b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5f65b-111">**Required/Optional**</span></span>|<span data-ttu-id="5f65b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5f65b-112">**Data Type**</span></span>|<span data-ttu-id="5f65b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f65b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f65b-114">_year_</span><span class="sxs-lookup"><span data-stu-id="5f65b-114">_year_</span></span> <br/> |<span data-ttu-id="5f65b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5f65b-115">Required</span></span>  <br/> |<span data-ttu-id="5f65b-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5f65b-116">**Integer**</span></span> <br/> |<span data-ttu-id="5f65b-117">Das Jahr.</span><span class="sxs-lookup"><span data-stu-id="5f65b-117">The year.</span></span>  <br/> |
| <span data-ttu-id="5f65b-118">_Monat_</span><span class="sxs-lookup"><span data-stu-id="5f65b-118">_month_</span></span> <br/> |<span data-ttu-id="5f65b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5f65b-119">Required</span></span>  <br/> |<span data-ttu-id="5f65b-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5f65b-120">**Integer**</span></span> <br/> |<span data-ttu-id="5f65b-121">Der Monat.</span><span class="sxs-lookup"><span data-stu-id="5f65b-121">The month.</span></span>  <br/> |
| <span data-ttu-id="5f65b-122">_day_</span><span class="sxs-lookup"><span data-stu-id="5f65b-122">_day_</span></span> <br/> |<span data-ttu-id="5f65b-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5f65b-123">Required</span></span>  <br/> |<span data-ttu-id="5f65b-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5f65b-124">**Integer**</span></span> <br/> |<span data-ttu-id="5f65b-125">Der Tag.</span><span class="sxs-lookup"><span data-stu-id="5f65b-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="5f65b-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f65b-126">Example 1</span></span>

<span data-ttu-id="5f65b-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="5f65b-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="5f65b-128">Gibt den Wert zurück, der 07.06.99 darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f65b-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5f65b-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f65b-129">Example 2</span></span>

<span data-ttu-id="5f65b-130">DATE(1999,6,7) + 4 t.</span><span class="sxs-lookup"><span data-stu-id="5f65b-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="5f65b-131">Gibt den Wert zurück, der 11.06.99 darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f65b-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5f65b-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5f65b-132">Example 3</span></span>

<span data-ttu-id="5f65b-133">FORMAT(DATUM(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="5f65b-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="5f65b-134">Gibt den Wert zurück, der Dienstag, 14. Oktober 1999 darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f65b-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

