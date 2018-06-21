---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Rundet eine Zahl auf die durch AnzahlVonStellen dargestellte Präzision.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19797883"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="e379e-103">ROUND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e379e-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e379e-104">Rundet eine Zahl auf die durch *AnzahlVonStellen* dargestellte Präzision.</span><span class="sxs-lookup"><span data-stu-id="e379e-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e379e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e379e-105">Syntax</span></span>

<span data-ttu-id="e379e-106">ROUND (** *Anzahl* **, ** *AnzahlVonStellen* **)</span><span class="sxs-lookup"><span data-stu-id="e379e-106">ROUND(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e379e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e379e-107">Parameters</span></span>

|<span data-ttu-id="e379e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e379e-108">**Name**</span></span>|<span data-ttu-id="e379e-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e379e-109">**Required/Optional**</span></span>|<span data-ttu-id="e379e-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e379e-110">**Data Type**</span></span>|<span data-ttu-id="e379e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e379e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e379e-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="e379e-112">_number_</span></span> <br/> |<span data-ttu-id="e379e-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e379e-113">Required</span></span>  <br/> |<span data-ttu-id="e379e-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e379e-114">**Number**</span></span> <br/> |<span data-ttu-id="e379e-115">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="e379e-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="e379e-116">_AnzahlVonStellen_</span><span class="sxs-lookup"><span data-stu-id="e379e-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="e379e-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e379e-117">Required</span></span>  <br/> |<span data-ttu-id="e379e-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e379e-118">**Number**</span></span> <br/> |<span data-ttu-id="e379e-119">Die Anzahl der Dezimalstellen für den Grad der Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="e379e-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e379e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e379e-120">Remarks</span></span>

<span data-ttu-id="e379e-121">Wenn der _Wert von AnzahlVonStellen_ größer als 0 ist, wird die _Zahl_ durch _AnzahlVonStellen_ rechts vom Dezimalkomma gerundet.</span><span class="sxs-lookup"><span data-stu-id="e379e-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="e379e-122">Wenn _AnzahlVonStellen_ 0 ist, wird die _Zahl_ in eine ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="e379e-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="e379e-123">Wenn der _Wert von AnzahlVonStellen_ kleiner als 0 ist, wird die _Zahl_ durch _AnzahlVonStellen_ links vom Dezimalkomma gerundet.</span><span class="sxs-lookup"><span data-stu-id="e379e-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e379e-124">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e379e-124">Example 1</span></span>

<span data-ttu-id="e379e-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="e379e-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="e379e-126">Gibt 123,65 zurück.</span><span class="sxs-lookup"><span data-stu-id="e379e-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e379e-127">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e379e-127">Example 2</span></span>

<span data-ttu-id="e379e-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="e379e-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="e379e-129">Gibt 124 zurück.</span><span class="sxs-lookup"><span data-stu-id="e379e-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e379e-130">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e379e-130">Example 3</span></span>

<span data-ttu-id="e379e-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="e379e-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="e379e-132">Gibt 120 zurück.</span><span class="sxs-lookup"><span data-stu-id="e379e-132">Returns 120.</span></span>
  

