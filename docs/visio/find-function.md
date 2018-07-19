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
description: Sucht eine Zeichenfolge innerhalb einer anderen Zeichenfolge und gibt die Startposition der gesuchten relativ zu seiner Position in der Zeichenfolge, die er enthält Textzeichenfolge zurück.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797036"
---
# <a name="find-function"></a><span data-ttu-id="428fa-103">FIND Function</span><span class="sxs-lookup"><span data-stu-id="428fa-103">FIND Function</span></span>

<span data-ttu-id="428fa-104">Sucht eine Zeichenfolge innerhalb einer anderen Zeichenfolge und gibt die Startposition der gesuchten relativ zu seiner Position in der Zeichenfolge, die er enthält Textzeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="428fa-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="428fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="428fa-105">Syntax</span></span>

<span data-ttu-id="428fa-106">Suchen Sie nach (** *Suchtext* **, ** *Within_text* **, [** *Erstes_Zeichen* **], [** *Ignore_case* **])</span><span class="sxs-lookup"><span data-stu-id="428fa-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="428fa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="428fa-107">Parameters</span></span>

|<span data-ttu-id="428fa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="428fa-108">**Name**</span></span>|<span data-ttu-id="428fa-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="428fa-109">**Required/Optional**</span></span>|<span data-ttu-id="428fa-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="428fa-110">**Data Type**</span></span>|<span data-ttu-id="428fa-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="428fa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="428fa-112">_Suchtext_</span><span class="sxs-lookup"><span data-stu-id="428fa-112">_find_text_</span></span> <br/> |<span data-ttu-id="428fa-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="428fa-113">Required</span></span>  <br/> |<span data-ttu-id="428fa-114">**String**</span><span class="sxs-lookup"><span data-stu-id="428fa-114">**String**</span></span> <br/> |<span data-ttu-id="428fa-115">Die gesuchte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="428fa-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="428fa-116">_format_</span><span class="sxs-lookup"><span data-stu-id="428fa-116">_format_</span></span> <br/> |<span data-ttu-id="428fa-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="428fa-117">Required</span></span>  <br/> |<span data-ttu-id="428fa-118">**String**</span><span class="sxs-lookup"><span data-stu-id="428fa-118">**String**</span></span> <br/> |<span data-ttu-id="428fa-119">Die Zeichenfolge, die den gesuchten Text enthält.</span><span class="sxs-lookup"><span data-stu-id="428fa-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="428fa-120">_Erstes_Zeichen_</span><span class="sxs-lookup"><span data-stu-id="428fa-120">_start_num_</span></span> <br/> |<span data-ttu-id="428fa-121">Optional</span><span class="sxs-lookup"><span data-stu-id="428fa-121">Optional</span></span>  <br/> |<span data-ttu-id="428fa-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="428fa-122">**Number**</span></span> <br/> |<span data-ttu-id="428fa-123">Das Zeichen, für die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="428fa-123">The character at which to start the search.</span></span> <span data-ttu-id="428fa-124">Das erste Zeichen in _Within_text_ ist 1.</span><span class="sxs-lookup"><span data-stu-id="428fa-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="428fa-125">Wenn _Start_num_ nicht vorhanden ist, wird angenommen, 1 sein.</span><span class="sxs-lookup"><span data-stu-id="428fa-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="428fa-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="428fa-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="428fa-127">Optional</span><span class="sxs-lookup"><span data-stu-id="428fa-127">Optional</span></span>  <br/> |<span data-ttu-id="428fa-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="428fa-128">**Boolean**</span></span> <br/> |<span data-ttu-id="428fa-p102">In der Standardeinstellung ist bei der FIND-Funktion Groß- und Kleinschreibung zu beachten. Wenn die Groß- und Kleinschreibung ignoriert werden soll, legen Sie für dieses Argument den Wert TRUE fest.</span><span class="sxs-lookup"><span data-stu-id="428fa-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="428fa-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="428fa-131">Return value</span></span>

<span data-ttu-id="428fa-132">Zahl</span><span class="sxs-lookup"><span data-stu-id="428fa-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="428fa-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="428fa-133">Remarks</span></span>

<span data-ttu-id="428fa-134">Wenn mehrere Übereinstimmungen gefunden werden, gibt die FIND-Funktion die Anfangsposition der die erste Übereinstimmung in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="428fa-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="428fa-135">Das Argument _Suchtext_ berücksichtigt Zeichen als Platzhalter werden nicht.</span><span class="sxs-lookup"><span data-stu-id="428fa-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="428fa-136">Wenn _Suchtext_:</span><span class="sxs-lookup"><span data-stu-id="428fa-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="428fa-137">Ist leer (""), suchen entspricht das erste Zeichen in der Suchzeichenfolge (d. h., das Zeichen mit dem _Erstes_Zeichen_ oder 1).</span><span class="sxs-lookup"><span data-stu-id="428fa-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="428fa-138">Erscheint nicht in _Within_text_, FIND gibt die #VALUE!</span><span class="sxs-lookup"><span data-stu-id="428fa-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="428fa-139">Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="428fa-139">error value.</span></span> 
    
<span data-ttu-id="428fa-140">Wenn _Start_num_:</span><span class="sxs-lookup"><span data-stu-id="428fa-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="428fa-p105">nicht größer als 0 (null) ist, gibt FIND den Fehlerwert #WERT! zurück.</span><span class="sxs-lookup"><span data-stu-id="428fa-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="428fa-143">Ist größer als die Länge von _Text ist_, gibt die #VALUE!</span><span class="sxs-lookup"><span data-stu-id="428fa-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="428fa-144">Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="428fa-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="428fa-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="428fa-145">Example</span></span>

<span data-ttu-id="428fa-146">FIND ("2003","Januar 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="428fa-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="428fa-147">Gibt 12 zurück.</span><span class="sxs-lookup"><span data-stu-id="428fa-147">Returns 12.</span></span> 
  

