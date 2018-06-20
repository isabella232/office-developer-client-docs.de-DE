---
title: STRSAMEEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Bestimmt, ob zwei Zeichenfolgen identisch sind.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798212"
---
# <a name="strsameex-function"></a><span data-ttu-id="226e6-103">STRSAMEEX Function</span><span class="sxs-lookup"><span data-stu-id="226e6-103">STRSAMEEX Function</span></span>

<span data-ttu-id="226e6-104">Bestimmt, ob zwei Zeichenfolgen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="226e6-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="226e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="226e6-105">Syntax</span></span>

<span data-ttu-id="226e6-106">STRSAMEEX ("** *Zeichenfolge1* **","** *Zeichenfolge2* **", ** *LocaleID* **, ** *Flag* **)</span><span class="sxs-lookup"><span data-stu-id="226e6-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="226e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="226e6-107">Parameters</span></span>

|<span data-ttu-id="226e6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="226e6-108">**Name**</span></span>|<span data-ttu-id="226e6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="226e6-109">**Required/Optional**</span></span>|<span data-ttu-id="226e6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="226e6-110">**Data Type**</span></span>|<span data-ttu-id="226e6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="226e6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="226e6-112">_Zeichenfolge1_</span><span class="sxs-lookup"><span data-stu-id="226e6-112">_string1_</span></span> <br/> |<span data-ttu-id="226e6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="226e6-113">Required</span></span>  <br/> |<span data-ttu-id="226e6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="226e6-114">**String**</span></span> <br/> |<span data-ttu-id="226e6-115">Die erste zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="226e6-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="226e6-116">_Zeichenfolge2_</span><span class="sxs-lookup"><span data-stu-id="226e6-116">_string2_</span></span> <br/> |<span data-ttu-id="226e6-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="226e6-117">Required</span></span>  <br/> |<span data-ttu-id="226e6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="226e6-118">**String**</span></span> <br/> | <span data-ttu-id="226e6-119">Die zweite zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="226e6-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="226e6-120">_Gebietsschema-ID_</span><span class="sxs-lookup"><span data-stu-id="226e6-120">_localeID_</span></span> <br/> |<span data-ttu-id="226e6-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="226e6-121">Required</span></span>  <br/> |<span data-ttu-id="226e6-122">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="226e6-122">**Numeric**</span></span> <br/> |<span data-ttu-id="226e6-123">Der lokale ID-Code.</span><span class="sxs-lookup"><span data-stu-id="226e6-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="226e6-124">_Flag_</span><span class="sxs-lookup"><span data-stu-id="226e6-124">_flag_</span></span> <br/> |<span data-ttu-id="226e6-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="226e6-125">Required</span></span>  <br/> |<span data-ttu-id="226e6-126">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="226e6-126">**Numeric**</span></span> <br/> | <span data-ttu-id="226e6-127">Ein Bit, das den Typ des Vergleichs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="226e6-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="226e6-128">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="226e6-128">Return value</span></span>

<span data-ttu-id="226e6-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="226e6-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="226e6-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="226e6-130">Remarks</span></span>

<span data-ttu-id="226e6-131">STRSAMEEX gibt true, wenn beide Zeichenfolgen identisch sind, und FALSE, wenn sie nicht.</span><span class="sxs-lookup"><span data-stu-id="226e6-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="226e6-132">Verwenden Sie diese Funktion, wenn Sie Multibyte-Zeichenfolgen vergleichen oder Vergleiche durchführen, die Groß-/Kleinschreibung Regeln für ein bestimmtes Gebietsschema verwenden.</span><span class="sxs-lookup"><span data-stu-id="226e6-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="226e6-133">Sie können eine beliebige Kombination folgender Flags mit der STRGLEICHEX-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="226e6-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="226e6-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="226e6-134">**Flag**</span></span>|<span data-ttu-id="226e6-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="226e6-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="226e6-136">1</span><span class="sxs-lookup"><span data-stu-id="226e6-136">1</span></span>  <br/> |<span data-ttu-id="226e6-137">Groß- und Kleinschreibung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="226e6-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="226e6-138">2</span><span class="sxs-lookup"><span data-stu-id="226e6-138">2</span></span>  <br/> |<span data-ttu-id="226e6-139">Nicht-gesperrte Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="226e6-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="226e6-140">4</span><span class="sxs-lookup"><span data-stu-id="226e6-140">4</span></span>  <br/> |<span data-ttu-id="226e6-141">Symbole ignorieren.</span><span class="sxs-lookup"><span data-stu-id="226e6-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="226e6-142">4096</span><span class="sxs-lookup"><span data-stu-id="226e6-142">4096</span></span>  <br/> |<span data-ttu-id="226e6-143">Interpunktionszeichen wie Symbole behandeln.</span><span class="sxs-lookup"><span data-stu-id="226e6-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="226e6-144">65536</span><span class="sxs-lookup"><span data-stu-id="226e6-144">65536</span></span>  <br/> |<span data-ttu-id="226e6-145">Nicht zwischen Hiragana- und Katakana-Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="226e6-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="226e6-146">131072</span><span class="sxs-lookup"><span data-stu-id="226e6-146">131072</span></span>  <br/> |<span data-ttu-id="226e6-147">Nicht zwischen Einzel-Byte-Zeichen und dem gleichen Zeichen als Doppel-Byte-Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="226e6-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

