---
title: FIND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Sucht eine Textzeichenfolge, die in einer anderen Textzeichenfolge enthalten ist, und gibt die Anfangsposition der Textzeichenfolge zurück, die Sie relativ zu ihrer Position in der Textzeichenfolge, die Sie enthält, suchen.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426576"
---
# <a name="find-function"></a><span data-ttu-id="aa1f4-103">FIND Function</span><span class="sxs-lookup"><span data-stu-id="aa1f4-103">FIND Function</span></span>

<span data-ttu-id="aa1f4-104">Sucht eine Textzeichenfolge, die in einer anderen Textzeichenfolge enthalten ist, und gibt die Anfangsposition der Textzeichenfolge zurück, die Sie relativ zu ihrer Position in der Textzeichenfolge, die Sie enthält, suchen.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aa1f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa1f4-105">Syntax</span></span>

<span data-ttu-id="aa1f4-106">Find (\* \* *Suchtext* \* \*, \* \* *within_text* \* *, [* \* *start_num* \* *], [* \* *ignore_case* \* \*])</span><span class="sxs-lookup"><span data-stu-id="aa1f4-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aa1f4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa1f4-107">Parameters</span></span>

|<span data-ttu-id="aa1f4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-108">**Name**</span></span>|<span data-ttu-id="aa1f4-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-109">**Required/Optional**</span></span>|<span data-ttu-id="aa1f4-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-110">**Data Type**</span></span>|<span data-ttu-id="aa1f4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aa1f4-112">_Suchtext_</span><span class="sxs-lookup"><span data-stu-id="aa1f4-112">_find_text_</span></span> <br/> |<span data-ttu-id="aa1f4-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="aa1f4-113">Required</span></span>  <br/> |<span data-ttu-id="aa1f4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-114">**String**</span></span> <br/> |<span data-ttu-id="aa1f4-115">Die gesuchte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="aa1f4-116">_format_</span><span class="sxs-lookup"><span data-stu-id="aa1f4-116">_format_</span></span> <br/> |<span data-ttu-id="aa1f4-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="aa1f4-117">Required</span></span>  <br/> |<span data-ttu-id="aa1f4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-118">**String**</span></span> <br/> |<span data-ttu-id="aa1f4-119">Die Zeichenfolge, die den gesuchten Text enthält.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="aa1f4-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="aa1f4-120">_start_num_</span></span> <br/> |<span data-ttu-id="aa1f4-121">Optional</span><span class="sxs-lookup"><span data-stu-id="aa1f4-121">Optional</span></span>  <br/> |<span data-ttu-id="aa1f4-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-122">**Number**</span></span> <br/> |<span data-ttu-id="aa1f4-123">Das Zeichen, bei dem die Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-123">The character at which to start the search.</span></span> <span data-ttu-id="aa1f4-124">Das erste Zeichen in _within_text_ ist 1.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="aa1f4-125">Wenn _start_num_ fehlt, wird davon ausgegangen, dass es 1 ist.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="aa1f4-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="aa1f4-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="aa1f4-127">Optional</span><span class="sxs-lookup"><span data-stu-id="aa1f4-127">Optional</span></span>  <br/> |<span data-ttu-id="aa1f4-128">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="aa1f4-128">**Boolean**</span></span> <br/> |<span data-ttu-id="aa1f4-129">In der Standardeinstellung ist bei der FIND-Funktion Groß- und Kleinschreibung zu beachten.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="aa1f4-130">Wenn die Groß- und Kleinschreibung ignoriert werden soll, legen Sie für dieses Argument den Wert TRUE fest.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aa1f4-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa1f4-131">Return value</span></span>

<span data-ttu-id="aa1f4-132">Zahl</span><span class="sxs-lookup"><span data-stu-id="aa1f4-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa1f4-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa1f4-133">Remarks</span></span>

<span data-ttu-id="aa1f4-134">Wenn mehrere Übereinstimmungen gefunden werden, gibt FIND die Anfangsposition der ersten Übereinstimmung in der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="aa1f4-135">Das _Suchtext_ -Argument berücksichtigt keine Zeichen als Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="aa1f4-136">If _Suchtext_:</span><span class="sxs-lookup"><span data-stu-id="aa1f4-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="aa1f4-137">Leer (""), sucht die Suche nach dem ersten Zeichen in der Suchzeichenfolge (das Zeichen _start_num_ oder 1).</span><span class="sxs-lookup"><span data-stu-id="aa1f4-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="aa1f4-138">Nicht in _within_text_angezeigt, gibt FIND den #VALUE zurück!</span><span class="sxs-lookup"><span data-stu-id="aa1f4-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="aa1f4-139">Ist dies nicht der Fall, gibt INDEX den Fehlerwert #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-139">error value.</span></span> 
    
<span data-ttu-id="aa1f4-140">If _start_num_:</span><span class="sxs-lookup"><span data-stu-id="aa1f4-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="aa1f4-141">nicht größer als 0 (null) ist, gibt FIND den Fehlerwert #WERT!</span><span class="sxs-lookup"><span data-stu-id="aa1f4-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="aa1f4-142">zurück.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-142">error value.</span></span> 
    
- <span data-ttu-id="aa1f4-143">Ist größer als die Länge von _within_text_, FINDreturns die #VALUE!</span><span class="sxs-lookup"><span data-stu-id="aa1f4-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="aa1f4-144">zurück.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="aa1f4-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa1f4-145">Example</span></span>

<span data-ttu-id="aa1f4-146">FIND ("2003","Januar 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="aa1f4-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="aa1f4-147">Gibt 12 zurück.</span><span class="sxs-lookup"><span data-stu-id="aa1f4-147">Returns 12.</span></span> 
  

