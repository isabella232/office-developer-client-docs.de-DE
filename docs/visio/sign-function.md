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
description: Gibt einen Wert, der die Zeichen einer Zahl darstellt.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798124"
---
# <a name="sign-function"></a><span data-ttu-id="61982-103">SIGN-Funktion</span><span class="sxs-lookup"><span data-stu-id="61982-103">SIGN Function</span></span>

<span data-ttu-id="61982-104">Gibt einen Wert, der die Zeichen einer Zahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="61982-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61982-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61982-105">Syntax</span></span>

<span data-ttu-id="61982-106">Vorzeichen (** *Anzahl* **, ** *mit zufälligen Daten* **)</span><span class="sxs-lookup"><span data-stu-id="61982-106">SIGN(** *number* **, ** *fuzz* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61982-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="61982-107">Parameters</span></span>

|<span data-ttu-id="61982-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="61982-108">**Name**</span></span>|<span data-ttu-id="61982-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="61982-109">**Required/Optional**</span></span>|<span data-ttu-id="61982-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="61982-110">**Data Type**</span></span>|<span data-ttu-id="61982-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61982-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61982-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="61982-112">_number_</span></span> <br/> |<span data-ttu-id="61982-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="61982-113">Required</span></span>  <br/> |<span data-ttu-id="61982-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="61982-114">**Numeric**</span></span> <br/> | <span data-ttu-id="61982-115">Die Zahl, für die das Vorzeichen bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61982-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="61982-116">_mit zufälligen Daten_</span><span class="sxs-lookup"><span data-stu-id="61982-116">_fuzz_</span></span> <br/> |<span data-ttu-id="61982-117">Optional</span><span class="sxs-lookup"><span data-stu-id="61982-117">Optional</span></span>  <br/> |<span data-ttu-id="61982-118">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="61982-118">**Numeric**</span></span> <br/> |<span data-ttu-id="61982-119">Gibt an, wie klein der Wert einer Zahl sein muss, damit diese als gleich 0 (null) betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="61982-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="61982-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="61982-120">Return value</span></span>

<span data-ttu-id="61982-121">Numeric</span><span class="sxs-lookup"><span data-stu-id="61982-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61982-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61982-122">Remarks</span></span>

<span data-ttu-id="61982-123">Die SIGN-Funktion gibt 1 zurück, wenn _Number_ positiv ist, 0, wenn die _Zahl_ 0 (null) oder-1 ist, ist _Zahl_ negativ.</span><span class="sxs-lookup"><span data-stu-id="61982-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="61982-124">Ein Wert _mit zufälligen Daten_ Specifyin hilft bei Fließkommazahlen vermieden, wenn eine Berechnung fast gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="61982-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="61982-125">Wenn Sie einen Wert _mit zufälligen Daten_ nicht angeben, verwendet Visio 1E-9 (0.000000001).</span><span class="sxs-lookup"><span data-stu-id="61982-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="61982-126">Sie möchten einen anderen Wert angeben, beim Skalieren von Zeichnungen, oder wenn Sie einen genauen Vergleich möchten.</span><span class="sxs-lookup"><span data-stu-id="61982-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="61982-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61982-127">Example 1</span></span>

<span data-ttu-id="61982-128">SIGN-5)</span><span class="sxs-lookup"><span data-stu-id="61982-128">SIGN(-5)</span></span>
  
<span data-ttu-id="61982-129">Gibt -1 zurück.</span><span class="sxs-lookup"><span data-stu-id="61982-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="61982-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="61982-130">Example 2</span></span>

<span data-ttu-id="61982-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="61982-131">SIGN(0)</span></span>
  
<span data-ttu-id="61982-132">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="61982-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="61982-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="61982-133">Example 3</span></span>

<span data-ttu-id="61982-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="61982-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="61982-135">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="61982-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="61982-136">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="61982-136">Example 4</span></span>

<span data-ttu-id="61982-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="61982-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="61982-138">Gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="61982-138">Returns 1.</span></span>
  

