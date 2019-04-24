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
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329792"
---
# <a name="strsameex-function"></a><span data-ttu-id="2f69b-103">STRSAMEEX Function</span><span class="sxs-lookup"><span data-stu-id="2f69b-103">STRSAMEEX Function</span></span>

<span data-ttu-id="2f69b-104">Bestimmt, ob zwei Zeichenfolgen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="2f69b-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2f69b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f69b-105">Syntax</span></span>

<span data-ttu-id="2f69b-106">STRSAMEEX ("\* \* *string1* \* *", "* \* *string2* \* \*", \* \* *Gebietsschema* -Nr. \* \*, \* \* *Flag* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2f69b-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2f69b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f69b-107">Parameters</span></span>

|<span data-ttu-id="2f69b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2f69b-108">**Name**</span></span>|<span data-ttu-id="2f69b-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2f69b-109">**Required/Optional**</span></span>|<span data-ttu-id="2f69b-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2f69b-110">**Data Type**</span></span>|<span data-ttu-id="2f69b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f69b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2f69b-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="2f69b-112">_string1_</span></span> <br/> |<span data-ttu-id="2f69b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2f69b-113">Required</span></span>  <br/> |<span data-ttu-id="2f69b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2f69b-114">**String**</span></span> <br/> |<span data-ttu-id="2f69b-115">Die erste zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2f69b-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="2f69b-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="2f69b-116">_string2_</span></span> <br/> |<span data-ttu-id="2f69b-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2f69b-117">Required</span></span>  <br/> |<span data-ttu-id="2f69b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="2f69b-118">**String**</span></span> <br/> | <span data-ttu-id="2f69b-119">Die zweite zu vergleichende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2f69b-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="2f69b-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="2f69b-120">_localeID_</span></span> <br/> |<span data-ttu-id="2f69b-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2f69b-121">Required</span></span>  <br/> |<span data-ttu-id="2f69b-122">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="2f69b-122">**Numeric**</span></span> <br/> |<span data-ttu-id="2f69b-123">Der lokale ID-Code.</span><span class="sxs-lookup"><span data-stu-id="2f69b-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="2f69b-124">_Flag_</span><span class="sxs-lookup"><span data-stu-id="2f69b-124">_flag_</span></span> <br/> |<span data-ttu-id="2f69b-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2f69b-125">Required</span></span>  <br/> |<span data-ttu-id="2f69b-126">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="2f69b-126">**Numeric**</span></span> <br/> | <span data-ttu-id="2f69b-127">Ein Bit, das den Typ des Vergleichs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2f69b-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2f69b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f69b-128">Return value</span></span>

<span data-ttu-id="2f69b-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="2f69b-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f69b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f69b-130">Remarks</span></span>

<span data-ttu-id="2f69b-131">STRSAMEEX gibt TRUE zurück, wenn beide Eingabezeichenfolgen identisch sind, und FALSE, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="2f69b-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="2f69b-132">Mit dieser Funktion können Sie Multi-Byte-Zeichenfolgenvergleichen oder Vergleiche ausführen, die Fall Regeln für ein bestimmtes Gebietsschema verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f69b-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="2f69b-133">Sie können eine beliebige Kombination folgender Flags mit der STRGLEICHEX-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f69b-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="2f69b-134">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f69b-134">**Flag**</span></span>|<span data-ttu-id="2f69b-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f69b-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f69b-136">1</span><span class="sxs-lookup"><span data-stu-id="2f69b-136">1</span></span>  <br/> |<span data-ttu-id="2f69b-137">Groß- und Kleinschreibung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2f69b-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="2f69b-138">2</span><span class="sxs-lookup"><span data-stu-id="2f69b-138">2</span></span>  <br/> |<span data-ttu-id="2f69b-139">Nicht-gesperrte Zeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2f69b-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="2f69b-140">4</span><span class="sxs-lookup"><span data-stu-id="2f69b-140">4</span></span>  <br/> |<span data-ttu-id="2f69b-141">Symbole ignorieren.</span><span class="sxs-lookup"><span data-stu-id="2f69b-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="2f69b-142">4096</span><span class="sxs-lookup"><span data-stu-id="2f69b-142">4096</span></span>  <br/> |<span data-ttu-id="2f69b-143">Interpunktionszeichen wie Symbole behandeln.</span><span class="sxs-lookup"><span data-stu-id="2f69b-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="2f69b-144">65536</span><span class="sxs-lookup"><span data-stu-id="2f69b-144">65536</span></span>  <br/> |<span data-ttu-id="2f69b-145">Nicht zwischen Hiragana- und Katakana-Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2f69b-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="2f69b-146">131072</span><span class="sxs-lookup"><span data-stu-id="2f69b-146">131072</span></span>  <br/> |<span data-ttu-id="2f69b-147">Nicht zwischen Einzel-Byte-Zeichen und dem gleichen Zeichen als Doppel-Byte-Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2f69b-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

