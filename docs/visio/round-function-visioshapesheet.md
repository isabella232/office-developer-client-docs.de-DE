---
title: ROUND-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Rundet eine Zahl auf die Genauigkeit, die durch numberofdigits dargestellt wird.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439968"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="60360-103">ROUND-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="60360-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="60360-104">Rundet eine Zahl auf die Genauigkeit, die durch *numberofdigits dargestellt wird.*</span><span class="sxs-lookup"><span data-stu-id="60360-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="60360-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60360-105">Syntax</span></span>

<span data-ttu-id="60360-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span><span class="sxs-lookup"><span data-stu-id="60360-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="60360-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="60360-107">Parameters</span></span>

|<span data-ttu-id="60360-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="60360-108">**Name**</span></span>|<span data-ttu-id="60360-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="60360-109">**Required/Optional**</span></span>|<span data-ttu-id="60360-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="60360-110">**Data Type**</span></span>|<span data-ttu-id="60360-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60360-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="60360-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="60360-112">_number_</span></span> <br/> |<span data-ttu-id="60360-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="60360-113">Required</span></span>  <br/> |<span data-ttu-id="60360-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="60360-114">**Number**</span></span> <br/> |<span data-ttu-id="60360-115">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="60360-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="60360-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="60360-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="60360-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="60360-117">Required</span></span>  <br/> |<span data-ttu-id="60360-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="60360-118">**Number**</span></span> <br/> |<span data-ttu-id="60360-119">Die Anzahl der Dezimalstellen für den Grad der Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="60360-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60360-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60360-120">Remarks</span></span>

<span data-ttu-id="60360-121">Wenn  _numberofdigits_ größer als 0 ist, wird  _zahl_  _durch numberofdigits_ rechts neben dem Dezimalkomma gerundet.</span><span class="sxs-lookup"><span data-stu-id="60360-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="60360-122">Wenn  _numberofdigits_ 0 ist,  _wird zahl_ auf eine ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="60360-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="60360-123">Wenn  _numberofdigits_ kleiner als 0 ist, wird  _zahl_ links vom Dezimalkomma  _durch numberofdigits_ gerundet.</span><span class="sxs-lookup"><span data-stu-id="60360-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="60360-124">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60360-124">Example 1</span></span>

<span data-ttu-id="60360-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="60360-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="60360-126">Gibt 123,65 zurück.</span><span class="sxs-lookup"><span data-stu-id="60360-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="60360-127">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="60360-127">Example 2</span></span>

<span data-ttu-id="60360-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="60360-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="60360-129">Gibt 124 zurück.</span><span class="sxs-lookup"><span data-stu-id="60360-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="60360-130">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="60360-130">Example 3</span></span>

<span data-ttu-id="60360-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="60360-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="60360-132">Gibt 120 zurück.</span><span class="sxs-lookup"><span data-stu-id="60360-132">Returns 120.</span></span>
  

