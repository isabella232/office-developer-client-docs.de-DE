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
description: Gibt das durch Jahr, Monat und Tag dargestellte Datum zurück, das gemäß der Formatvorlage für kurzes Datum in den regionalen Einstellungen des Systems formatiert ist. Die Werte für Jahr, Monat und Tag entsprechen dem gregorianischen Kalender.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360333"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="53979-104">DATE-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="53979-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="53979-105">Gibt das durch *Jahr, Monat* und *Tag* dargestellte Datum zurück, das gemäß der Formatvorlage für kurzes Datum in den regionalen Einstellungen des Systems formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="53979-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="53979-106">Die Werte für *Jahr*, *Monat* und *Tag* entsprechen dem gregorianischen Kalender.</span><span class="sxs-lookup"><span data-stu-id="53979-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53979-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53979-107">Syntax</span></span>

<span data-ttu-id="53979-108">Datum (\* \* *Jahr* \* \*, \* \* *Monat* \* \*, \* \* *Tag* \* \*)</span><span class="sxs-lookup"><span data-stu-id="53979-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="53979-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="53979-109">Parameters</span></span>

|<span data-ttu-id="53979-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="53979-110">**Name**</span></span>|<span data-ttu-id="53979-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="53979-111">**Required/Optional**</span></span>|<span data-ttu-id="53979-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="53979-112">**Data Type**</span></span>|<span data-ttu-id="53979-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53979-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="53979-114">_year_</span><span class="sxs-lookup"><span data-stu-id="53979-114">_year_</span></span> <br/> |<span data-ttu-id="53979-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="53979-115">Required</span></span>  <br/> |<span data-ttu-id="53979-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="53979-116">**Integer**</span></span> <br/> |<span data-ttu-id="53979-117">Das Jahr.</span><span class="sxs-lookup"><span data-stu-id="53979-117">The year.</span></span>  <br/> |
| <span data-ttu-id="53979-118">_Monat_</span><span class="sxs-lookup"><span data-stu-id="53979-118">_month_</span></span> <br/> |<span data-ttu-id="53979-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="53979-119">Required</span></span>  <br/> |<span data-ttu-id="53979-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="53979-120">**Integer**</span></span> <br/> |<span data-ttu-id="53979-121">Der Monat.</span><span class="sxs-lookup"><span data-stu-id="53979-121">The month.</span></span>  <br/> |
| <span data-ttu-id="53979-122">_day_</span><span class="sxs-lookup"><span data-stu-id="53979-122">_day_</span></span> <br/> |<span data-ttu-id="53979-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="53979-123">Required</span></span>  <br/> |<span data-ttu-id="53979-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="53979-124">**Integer**</span></span> <br/> |<span data-ttu-id="53979-125">Der Tag.</span><span class="sxs-lookup"><span data-stu-id="53979-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="53979-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53979-126">Example 1</span></span>

<span data-ttu-id="53979-127">DATUM (1999, 6, 7)</span><span class="sxs-lookup"><span data-stu-id="53979-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="53979-128">Gibt den Wert zurück, der 07.06.99 darstellt.</span><span class="sxs-lookup"><span data-stu-id="53979-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="53979-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53979-129">Example 2</span></span>

<span data-ttu-id="53979-130">DATE(1999,6,7) + 4 t.</span><span class="sxs-lookup"><span data-stu-id="53979-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="53979-131">Gibt den Wert zurück, der 11.06.99 darstellt.</span><span class="sxs-lookup"><span data-stu-id="53979-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="53979-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="53979-132">Example 3</span></span>

<span data-ttu-id="53979-133">FORMAT (DATUM (1999, 10, 14), "C")</span><span class="sxs-lookup"><span data-stu-id="53979-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="53979-134">Gibt den Wert zurück, der Dienstag, 14. Oktober 1999 darstellt.</span><span class="sxs-lookup"><span data-stu-id="53979-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

