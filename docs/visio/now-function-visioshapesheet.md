---
title: NOW-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Gibt den aktuellen Wert für Datum und Uhrzeit zurück.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340992"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="27d60-103">NOW-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="27d60-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="27d60-104">Gibt den aktuellen Wert für Datum und Uhrzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="27d60-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="27d60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27d60-105">Syntax</span></span>

<span data-ttu-id="27d60-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="27d60-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="27d60-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27d60-107">Return value</span></span>

<span data-ttu-id="27d60-108">DateTime</span><span class="sxs-lookup"><span data-stu-id="27d60-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27d60-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27d60-109">Remarks</span></span>

<span data-ttu-id="27d60-110">NOW wird in Abständen von einer Minute jeweils neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="27d60-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="27d60-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27d60-111">Example 1</span></span>

<span data-ttu-id="27d60-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="27d60-112">NOW( )</span></span>
  
<span data-ttu-id="27d60-113">Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück, z. B. 27.9.2010 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="27d60-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="27d60-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="27d60-114">Example 2</span></span>

<span data-ttu-id="27d60-115">FORMAT(JETZT(),"tt MMM. jjjj hh:mm")</span><span class="sxs-lookup"><span data-stu-id="27d60-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="27d60-116">Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück, formatiert als 27 Sep. 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="27d60-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="27d60-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="27d60-117">Example 3</span></span>

<span data-ttu-id="27d60-118">NOW () + 2EW.</span><span class="sxs-lookup"><span data-stu-id="27d60-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="27d60-119">Gibt das aktuelle Datum und die aktuelle Uhrzeit plus zwei vergangene Wochen zurück, z. B. 11.10.10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="27d60-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

