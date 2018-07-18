---
title: STRSAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Bestimmt, ob die Zeichenfolgen identisch sind. Es gibt TRUE zurück, wenn sie identisch sind, und FALSE, wenn sie nicht.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798190"
---
# <a name="strsame-function"></a><span data-ttu-id="ebc41-104">STRSAME Function</span><span class="sxs-lookup"><span data-stu-id="ebc41-104">STRSAME Function</span></span>

<span data-ttu-id="ebc41-105">Bestimmt, ob die Zeichenfolgen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ebc41-105">Determines whether strings are the same.</span></span> <span data-ttu-id="ebc41-106">Es gibt TRUE zurück, wenn sie identisch sind, und FALSE, wenn sie nicht.</span><span class="sxs-lookup"><span data-stu-id="ebc41-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ebc41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebc41-107">Syntax</span></span>

<span data-ttu-id="ebc41-108">STRSAME ("** *Zeichenfolge1* **","** *Zeichenfolge2* **", ** *IgnoreCase* **)</span><span class="sxs-lookup"><span data-stu-id="ebc41-108">STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ebc41-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebc41-109">Parameters</span></span>

|<span data-ttu-id="ebc41-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ebc41-110">**Name**</span></span>|<span data-ttu-id="ebc41-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ebc41-111">**Required/Optional**</span></span>|<span data-ttu-id="ebc41-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ebc41-112">**Data Type**</span></span>|<span data-ttu-id="ebc41-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebc41-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ebc41-114">_Zeichenfolge1_</span><span class="sxs-lookup"><span data-stu-id="ebc41-114">_string1_</span></span> <br/> |<span data-ttu-id="ebc41-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebc41-115">Required</span></span>  <br/> |<span data-ttu-id="ebc41-116">**String**</span><span class="sxs-lookup"><span data-stu-id="ebc41-116">**String**</span></span> <br/> |<span data-ttu-id="ebc41-117">Die erste zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ebc41-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="ebc41-118">_Zeichenfolge2_</span><span class="sxs-lookup"><span data-stu-id="ebc41-118">_string2_</span></span> <br/> |<span data-ttu-id="ebc41-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebc41-119">Required</span></span>  <br/> |<span data-ttu-id="ebc41-120">**String**</span><span class="sxs-lookup"><span data-stu-id="ebc41-120">**String**</span></span> <br/> |<span data-ttu-id="ebc41-121">Die zweite zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ebc41-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="ebc41-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="ebc41-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="ebc41-123">Optional</span><span class="sxs-lookup"><span data-stu-id="ebc41-123">Optional</span></span>  <br/> |<span data-ttu-id="ebc41-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ebc41-124">**Boolean**</span></span> <br/> |<span data-ttu-id="ebc41-p103">TRUE steht für "Groß- und Kleinschreibung ignorieren" und FALSE für "Groß- und Kleinschreibung berücksichtigen". Die Standardeinstellung ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="ebc41-p103">TRUE to ignore the case and FALSE to compare the case. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ebc41-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ebc41-127">Return value</span></span>

<span data-ttu-id="ebc41-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="ebc41-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebc41-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebc41-129">Remarks</span></span>

<span data-ttu-id="ebc41-130">Wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche mit Groß- und Kleinschreibregeln für ein bestimmtes Gebietsschema durchführen möchten, verwenden Sie die STRSAMEEX-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ebc41-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ebc41-131">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebc41-131">Example 1</span></span>

<span data-ttu-id="ebc41-132">STRSAME("Katze","Hund")</span><span class="sxs-lookup"><span data-stu-id="ebc41-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="ebc41-133">Gibt FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ebc41-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ebc41-134">Example 2</span></span>

<span data-ttu-id="ebc41-135">STRSAME("Katze","Katze")</span><span class="sxs-lookup"><span data-stu-id="ebc41-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="ebc41-136">Gibt TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ebc41-137">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ebc41-137">Example 3</span></span>

<span data-ttu-id="ebc41-138">STRSAME("Katze","Katze", WAHR)</span><span class="sxs-lookup"><span data-stu-id="ebc41-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="ebc41-139">Gibt TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="ebc41-140">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ebc41-140">Example 4</span></span>

<span data-ttu-id="ebc41-141">STRSAME("katze","KATZE")</span><span class="sxs-lookup"><span data-stu-id="ebc41-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="ebc41-142">Gibt FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="ebc41-143">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ebc41-143">Example 5</span></span>

<span data-ttu-id="ebc41-144">STRSAME("katze","KATZE", WAHR)</span><span class="sxs-lookup"><span data-stu-id="ebc41-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="ebc41-145">Gibt TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="ebc41-146">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="ebc41-146">Example 6</span></span>

<span data-ttu-id="ebc41-147">STRSAME("kätze","KATZE", WAHR)</span><span class="sxs-lookup"><span data-stu-id="ebc41-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="ebc41-148">Gibt FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="ebc41-149">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="ebc41-149">Example 7</span></span>

<span data-ttu-id="ebc41-150">STRSAME("kätze","KÄTZE", WAHR)</span><span class="sxs-lookup"><span data-stu-id="ebc41-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="ebc41-151">Gibt TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="ebc41-151">Returns TRUE.</span></span>
  

