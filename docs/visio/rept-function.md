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
description: Wiederholt Text so oft wie angegeben.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412079"
---
# <a name="rept-function"></a><span data-ttu-id="9d127-103">REPT Function</span><span class="sxs-lookup"><span data-stu-id="9d127-103">REPT Function</span></span>

<span data-ttu-id="9d127-104">Wiederholt Text so oft wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="9d127-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9d127-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d127-105">Syntax</span></span>

<span data-ttu-id="9d127-106">REPT (\* \* *Text* \* \*, \* \* *Multiplikator* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9d127-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9d127-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d127-107">Parameters</span></span>

|<span data-ttu-id="9d127-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9d127-108">**Name**</span></span>|<span data-ttu-id="9d127-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9d127-109">**Required/Optional**</span></span>|<span data-ttu-id="9d127-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9d127-110">**Data Type**</span></span>|<span data-ttu-id="9d127-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d127-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9d127-112">_text_</span><span class="sxs-lookup"><span data-stu-id="9d127-112">_text_</span></span> <br/> |<span data-ttu-id="9d127-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9d127-113">Required</span></span>  <br/> |<span data-ttu-id="9d127-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9d127-114">**String**</span></span> <br/> | <span data-ttu-id="9d127-115">Der Text, der wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d127-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="9d127-116">_Multiplikator_</span><span class="sxs-lookup"><span data-stu-id="9d127-116">_number_times_</span></span> <br/> |<span data-ttu-id="9d127-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9d127-117">Required</span></span>  <br/> |<span data-ttu-id="9d127-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="9d127-118">**Number**</span></span> <br/> |<span data-ttu-id="9d127-119">Eine positive Zahl, die angibt, wie oft der Text wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d127-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d127-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d127-120">Remarks</span></span>

<span data-ttu-id="9d127-121">Wenn *Multiplikator* ist:</span><span class="sxs-lookup"><span data-stu-id="9d127-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="9d127-122">Null (0) ist, gibt REPT "" (leeren Text) zurück.</span><span class="sxs-lookup"><span data-stu-id="9d127-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="9d127-123">keine Ganzzahl ist, wird es abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9d127-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="9d127-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9d127-124">Example</span></span>

<span data-ttu-id="9d127-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="9d127-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="9d127-126">Gibt \* \* \*zurück \*. \*</span><span class="sxs-lookup"><span data-stu-id="9d127-126">Returns \*\*\*\*\*.</span></span> 
  

