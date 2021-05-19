---
title: SIGN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Gibt einen Wert zurück, der das Vorzeichen einer Zahl darstellt.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420654"
---
# <a name="sign-function"></a><span data-ttu-id="70299-103">SIGN Function</span><span class="sxs-lookup"><span data-stu-id="70299-103">SIGN Function</span></span>

<span data-ttu-id="70299-104">Gibt einen Wert zurück, der das Vorzeichen einer Zahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="70299-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="70299-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70299-105">Syntax</span></span>

<span data-ttu-id="70299-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span><span class="sxs-lookup"><span data-stu-id="70299-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="70299-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="70299-107">Parameters</span></span>

|<span data-ttu-id="70299-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="70299-108">**Name**</span></span>|<span data-ttu-id="70299-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="70299-109">**Required/Optional**</span></span>|<span data-ttu-id="70299-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="70299-110">**Data Type**</span></span>|<span data-ttu-id="70299-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70299-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="70299-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="70299-112">_number_</span></span> <br/> |<span data-ttu-id="70299-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="70299-113">Required</span></span>  <br/> |<span data-ttu-id="70299-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="70299-114">**Numeric**</span></span> <br/> | <span data-ttu-id="70299-115">Die Zahl, für die das Vorzeichen bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70299-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="70299-116">_fuzz_</span><span class="sxs-lookup"><span data-stu-id="70299-116">_fuzz_</span></span> <br/> |<span data-ttu-id="70299-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="70299-117">Optional</span></span>  <br/> |<span data-ttu-id="70299-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="70299-118">**Numeric**</span></span> <br/> |<span data-ttu-id="70299-119">Gibt an, wie klein der Wert einer Zahl sein muss, damit diese als gleich 0 (null) betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="70299-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="70299-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70299-120">Return value</span></span>

<span data-ttu-id="70299-121">Numeric</span><span class="sxs-lookup"><span data-stu-id="70299-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70299-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70299-122">Remarks</span></span>

<span data-ttu-id="70299-123">Die SIGN-Funktion gibt 1 zurück, wenn  _Zahl_ positiv ist, 0, wenn  _Zahl_ null ist, oder -1, wenn  _Zahl_ negativ ist.</span><span class="sxs-lookup"><span data-stu-id="70299-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="70299-124">Das Angeben eines  _Fuzz-Werts_ hilft, Gleitkomma-Roundofffehler zu vermeiden, wenn eine Berechnung fast null ist.</span><span class="sxs-lookup"><span data-stu-id="70299-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="70299-125">Wenn Sie keinen _Fuzz-Wert_ angeben, Visio 1E-9 (0,00000000001) verwendet.</span><span class="sxs-lookup"><span data-stu-id="70299-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="70299-126">Sie können bei Bedarf einen anderen Wert angeben, wenn Sie Zeichnungen skalieren möchten oder einen exakten Vergleich anstreben.</span><span class="sxs-lookup"><span data-stu-id="70299-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="70299-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70299-127">Example 1</span></span>

<span data-ttu-id="70299-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="70299-128">SIGN(-5)</span></span>
  
<span data-ttu-id="70299-129">Gibt -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="70299-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="70299-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="70299-130">Example 2</span></span>

<span data-ttu-id="70299-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="70299-131">SIGN(0)</span></span>
  
<span data-ttu-id="70299-132">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="70299-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="70299-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="70299-133">Example 3</span></span>

<span data-ttu-id="70299-134">SIGN(0.000000000001)</span><span class="sxs-lookup"><span data-stu-id="70299-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="70299-135">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="70299-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="70299-136">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="70299-136">Example 4</span></span>

<span data-ttu-id="70299-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="70299-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="70299-138">Gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="70299-138">Returns 1.</span></span>
  

