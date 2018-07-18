---
title: NOW Function (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Gibt den aktuellen Wert für Datum und Uhrzeit zurück.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797577"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="98008-103">NOW Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="98008-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="98008-104">Gibt den aktuellen Wert für Datum und Uhrzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="98008-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="98008-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98008-105">Syntax</span></span>

<span data-ttu-id="98008-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="98008-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="98008-107">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="98008-107">Return value</span></span>

<span data-ttu-id="98008-108">Datetime</span><span class="sxs-lookup"><span data-stu-id="98008-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98008-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98008-109">Remarks</span></span>

<span data-ttu-id="98008-110">NOW wird in Abständen von einer Minute jeweils neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="98008-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="98008-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98008-111">Example 1</span></span>

<span data-ttu-id="98008-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="98008-112">NOW( )</span></span>
  
<span data-ttu-id="98008-113">Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück, z. B. 27.9.2010 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="98008-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="98008-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="98008-114">Example 2</span></span>

<span data-ttu-id="98008-115">FORMAT(JETZT(),"tt MMM. jjjj hh:mm")</span><span class="sxs-lookup"><span data-stu-id="98008-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="98008-116">Gibt das aktuelle Datum und die aktuelle Uhrzeit zurück, formatiert als 27 Sep. 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="98008-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="98008-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="98008-117">Example 3</span></span>

<span data-ttu-id="98008-118">NOW()+2EW.</span><span class="sxs-lookup"><span data-stu-id="98008-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="98008-119">Gibt das aktuelle Datum und die aktuelle Uhrzeit plus zwei vergangene Wochen zurück, z. B. 11.10.10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="98008-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

