---
title: REPT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Wiederholt den Text eine angegebene Anzahl von Malen.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797874"
---
# <a name="rept-function"></a><span data-ttu-id="e15e8-103">REPT Function</span><span class="sxs-lookup"><span data-stu-id="e15e8-103">REPT Function</span></span>

<span data-ttu-id="e15e8-104">Wiederholt den Text eine angegebene Anzahl von Malen.</span><span class="sxs-lookup"><span data-stu-id="e15e8-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e15e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e15e8-105">Syntax</span></span>

<span data-ttu-id="e15e8-106">REPT (** *Text* **, ** *Zahl_Wiederholungen* **)</span><span class="sxs-lookup"><span data-stu-id="e15e8-106">REPT (** *text* **, ** *number_times* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e15e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e15e8-107">Parameters</span></span>

|<span data-ttu-id="e15e8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e15e8-108">**Name**</span></span>|<span data-ttu-id="e15e8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e15e8-109">**Required/Optional**</span></span>|<span data-ttu-id="e15e8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e15e8-110">**Data Type**</span></span>|<span data-ttu-id="e15e8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e15e8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e15e8-112">_text_</span><span class="sxs-lookup"><span data-stu-id="e15e8-112">_text_</span></span> <br/> |<span data-ttu-id="e15e8-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e15e8-113">Required</span></span>  <br/> |<span data-ttu-id="e15e8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e15e8-114">**String**</span></span> <br/> | <span data-ttu-id="e15e8-115">Der Text, der wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e15e8-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="e15e8-116">_Zahl_Wiederholungen_</span><span class="sxs-lookup"><span data-stu-id="e15e8-116">_number_times_</span></span> <br/> |<span data-ttu-id="e15e8-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e15e8-117">Required</span></span>  <br/> |<span data-ttu-id="e15e8-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e15e8-118">**Number**</span></span> <br/> |<span data-ttu-id="e15e8-119">Eine positive Zahl, die angibt, wie oft der Text wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e15e8-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e15e8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e15e8-120">Remarks</span></span>

<span data-ttu-id="e15e8-121">Wenn *number_times:*</span><span class="sxs-lookup"><span data-stu-id="e15e8-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="e15e8-122">Null (0) ist, gibt REPT "" (leeren Text) zurück.</span><span class="sxs-lookup"><span data-stu-id="e15e8-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="e15e8-123">keine Ganzzahl ist, wird es abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="e15e8-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="e15e8-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e15e8-124">Example</span></span>

<span data-ttu-id="e15e8-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="e15e8-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="e15e8-126">Gibt \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="e15e8-126">Returns \*\*\*\*\*.</span></span> 
  

