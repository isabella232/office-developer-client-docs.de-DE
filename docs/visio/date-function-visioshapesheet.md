---
title: DATE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Gibt das Durch Jahr, Monat und Tag dargestellte Datum zurück, das gemäß der kurzen Datumsart im regionalen Format des Systems Einstellungen. Die Werte für Jahr, Monat und Tag spiegeln den gregorianischen Kalender wider.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360333"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="a30d3-104">DATE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a30d3-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a30d3-105">Gibt das Durch Jahr, Monat  und Tag dargestellte Datum *zurück,* das gemäß der kurzen Datumsart im regionalen Format des Systems Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a30d3-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="a30d3-106">Die Werte für  *Jahr,* *Monat*  und  *Tag spiegeln*  den gregorianischen Kalender wider.</span><span class="sxs-lookup"><span data-stu-id="a30d3-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a30d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a30d3-107">Syntax</span></span>

<span data-ttu-id="a30d3-108">DATE(\*\* *Jahr* \*\*, \*\* *Monat* \*\*, \*\* *Tag* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a30d3-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a30d3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a30d3-109">Parameters</span></span>

|<span data-ttu-id="a30d3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a30d3-110">**Name**</span></span>|<span data-ttu-id="a30d3-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a30d3-111">**Required/Optional**</span></span>|<span data-ttu-id="a30d3-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a30d3-112">**Data Type**</span></span>|<span data-ttu-id="a30d3-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a30d3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a30d3-114">_year_</span><span class="sxs-lookup"><span data-stu-id="a30d3-114">_year_</span></span> <br/> |<span data-ttu-id="a30d3-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a30d3-115">Required</span></span>  <br/> |<span data-ttu-id="a30d3-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a30d3-116">**Integer**</span></span> <br/> |<span data-ttu-id="a30d3-117">Das Jahr.</span><span class="sxs-lookup"><span data-stu-id="a30d3-117">The year.</span></span>  <br/> |
| <span data-ttu-id="a30d3-118">_Monat_</span><span class="sxs-lookup"><span data-stu-id="a30d3-118">_month_</span></span> <br/> |<span data-ttu-id="a30d3-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a30d3-119">Required</span></span>  <br/> |<span data-ttu-id="a30d3-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a30d3-120">**Integer**</span></span> <br/> |<span data-ttu-id="a30d3-121">Der Monat.</span><span class="sxs-lookup"><span data-stu-id="a30d3-121">The month.</span></span>  <br/> |
| <span data-ttu-id="a30d3-122">_day_</span><span class="sxs-lookup"><span data-stu-id="a30d3-122">_day_</span></span> <br/> |<span data-ttu-id="a30d3-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a30d3-123">Required</span></span>  <br/> |<span data-ttu-id="a30d3-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a30d3-124">**Integer**</span></span> <br/> |<span data-ttu-id="a30d3-125">Der Tag.</span><span class="sxs-lookup"><span data-stu-id="a30d3-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="a30d3-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a30d3-126">Example 1</span></span>

<span data-ttu-id="a30d3-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="a30d3-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="a30d3-128">Gibt den Wert zurück, der 07.06.99 darstellt.</span><span class="sxs-lookup"><span data-stu-id="a30d3-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a30d3-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a30d3-129">Example 2</span></span>

<span data-ttu-id="a30d3-130">DATE(1999,6,7) + 4 t.</span><span class="sxs-lookup"><span data-stu-id="a30d3-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="a30d3-131">Gibt den Wert zurück, der 11.06.99 darstellt.</span><span class="sxs-lookup"><span data-stu-id="a30d3-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a30d3-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a30d3-132">Example 3</span></span>

<span data-ttu-id="a30d3-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="a30d3-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="a30d3-134">Gibt den Wert zurück, der Dienstag, 14. Oktober 1999 darstellt.</span><span class="sxs-lookup"><span data-stu-id="a30d3-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

