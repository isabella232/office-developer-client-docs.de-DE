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
description: Gibt einen Wert zurück, der das Zeichen einer Zahl darstellt.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357456"
---
# <a name="sign-function"></a><span data-ttu-id="ad79c-103">SIGN Function</span><span class="sxs-lookup"><span data-stu-id="ad79c-103">SIGN Function</span></span>

<span data-ttu-id="ad79c-104">Gibt einen Wert zurück, der das Zeichen einer Zahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad79c-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ad79c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad79c-105">Syntax</span></span>

<span data-ttu-id="ad79c-106">SIGN (\* \* *Number* \* \*, \* \* *Fuzz* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ad79c-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ad79c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad79c-107">Parameters</span></span>

|<span data-ttu-id="ad79c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad79c-108">**Name**</span></span>|<span data-ttu-id="ad79c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ad79c-109">**Required/Optional**</span></span>|<span data-ttu-id="ad79c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ad79c-110">**Data Type**</span></span>|<span data-ttu-id="ad79c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad79c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ad79c-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="ad79c-112">_number_</span></span> <br/> |<span data-ttu-id="ad79c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ad79c-113">Required</span></span>  <br/> |<span data-ttu-id="ad79c-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="ad79c-114">**Numeric**</span></span> <br/> | <span data-ttu-id="ad79c-115">Die Zahl, für die das Vorzeichen bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad79c-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="ad79c-116">_Fuzz_</span><span class="sxs-lookup"><span data-stu-id="ad79c-116">_fuzz_</span></span> <br/> |<span data-ttu-id="ad79c-117">Optional</span><span class="sxs-lookup"><span data-stu-id="ad79c-117">Optional</span></span>  <br/> |<span data-ttu-id="ad79c-118">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="ad79c-118">**Numeric**</span></span> <br/> |<span data-ttu-id="ad79c-119">Gibt an, wie klein der Wert einer Zahl sein muss, damit diese als gleich 0 (null) betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="ad79c-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ad79c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad79c-120">Return value</span></span>

<span data-ttu-id="ad79c-121">Numerisch</span><span class="sxs-lookup"><span data-stu-id="ad79c-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad79c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad79c-122">Remarks</span></span>

<span data-ttu-id="ad79c-123">Die SIGN-Funktion gibt 1 zurück, wenn _Number_ positiv ist __ , 0, wenn Number gleich NULL ist, oder-1, wenn _Number_ negativ ist.</span><span class="sxs-lookup"><span data-stu-id="ad79c-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="ad79c-124">Angeben in ein _Fuzz_ -Wert hilft beim Vermeiden von Gleitkomma-Rundungs-Fehlern, wenn eine Berechnung fast null ist.</span><span class="sxs-lookup"><span data-stu-id="ad79c-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="ad79c-125">Wenn Sie keinen _Fuzz_ -Wert angeben, verwendet Visio 1E-9 (0,000000001).</span><span class="sxs-lookup"><span data-stu-id="ad79c-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="ad79c-126">Sie können bei Bedarf einen anderen Wert angeben, wenn Sie Zeichnungen skalieren möchten oder einen exakten Vergleich anstreben.</span><span class="sxs-lookup"><span data-stu-id="ad79c-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ad79c-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad79c-127">Example 1</span></span>

<span data-ttu-id="ad79c-128">SIGN (-5)</span><span class="sxs-lookup"><span data-stu-id="ad79c-128">SIGN(-5)</span></span>
  
<span data-ttu-id="ad79c-129">Gibt -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="ad79c-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ad79c-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ad79c-130">Example 2</span></span>

<span data-ttu-id="ad79c-131">SIGN (0)</span><span class="sxs-lookup"><span data-stu-id="ad79c-131">SIGN(0)</span></span>
  
<span data-ttu-id="ad79c-132">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="ad79c-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ad79c-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ad79c-133">Example 3</span></span>

<span data-ttu-id="ad79c-134">SIGN (0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="ad79c-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="ad79c-135">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="ad79c-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="ad79c-136">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ad79c-136">Example 4</span></span>

<span data-ttu-id="ad79c-137">SIGN (0.00000000001, 0)</span><span class="sxs-lookup"><span data-stu-id="ad79c-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="ad79c-138">Gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="ad79c-138">Returns 1.</span></span>
  

