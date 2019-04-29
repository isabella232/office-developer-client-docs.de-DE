---
title: TRUNC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern abgeschnitten wurde.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426499"
---
# <a name="trunc-function"></a><span data-ttu-id="88ad2-103">TRUNC Function</span><span class="sxs-lookup"><span data-stu-id="88ad2-103">TRUNC Function</span></span>

<span data-ttu-id="88ad2-104">Gibt eine Zahl zurück, die auf die angegebene Anzahl von Ziffern abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="88ad2-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="88ad2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88ad2-105">Syntax</span></span>

<span data-ttu-id="88ad2-106">KÜRZEN (\* \* *Number* \* \*, \* \* *Wert von AnzahlVonStellen* \* \*)</span><span class="sxs-lookup"><span data-stu-id="88ad2-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88ad2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="88ad2-107">Parameters</span></span>

|<span data-ttu-id="88ad2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="88ad2-108">**Name**</span></span>|<span data-ttu-id="88ad2-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="88ad2-109">**Required/Optional**</span></span>|<span data-ttu-id="88ad2-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="88ad2-110">**Data Type**</span></span>|<span data-ttu-id="88ad2-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88ad2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88ad2-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="88ad2-112">_number_</span></span> <br/> |<span data-ttu-id="88ad2-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="88ad2-113">Required</span></span>  <br/> |<span data-ttu-id="88ad2-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="88ad2-114">**Numeric**</span></span> <br/> |<span data-ttu-id="88ad2-115">Die zu kürzende Zahl.</span><span class="sxs-lookup"><span data-stu-id="88ad2-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="88ad2-116">_Wert von AnzahlVonStellen_</span><span class="sxs-lookup"><span data-stu-id="88ad2-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="88ad2-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="88ad2-117">Required</span></span>  <br/> |<span data-ttu-id="88ad2-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="88ad2-118">**Numeric**</span></span> <br/> |<span data-ttu-id="88ad2-119">Die Anzahl der Ziffern, auf die die _Zahl_gekürzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="88ad2-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="88ad2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88ad2-120">Return value</span></span>

<span data-ttu-id="88ad2-121">Numerischen.</span><span class="sxs-lookup"><span data-stu-id="88ad2-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88ad2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88ad2-122">Remarks</span></span>

<span data-ttu-id="88ad2-123">Wenn _Wert von AnzahlVonStellen_ größer als 0 ist, wird die _Zahl_ auf _Wert von AnzahlVonStellen_ rechts vom Dezimaltrennzeichen abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="88ad2-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="88ad2-124">Wenn _Wert von AnzahlVonStellen_ 0 ist, wird _Number_ auf eine ganze Zahl gekürzt.</span><span class="sxs-lookup"><span data-stu-id="88ad2-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="88ad2-125">Wenn _Wert von AnzahlVonStellen_ kleiner als 0 ist, wird die _Zahl_ auf _Wert von AnzahlVonStellen_ Links vom Dezimaltrennzeichen abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="88ad2-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="88ad2-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88ad2-126">Example 1</span></span>

<span data-ttu-id="88ad2-127">KÜRZEN (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="88ad2-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="88ad2-128">Gibt 123,65 zurück.</span><span class="sxs-lookup"><span data-stu-id="88ad2-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="88ad2-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="88ad2-129">Example 2</span></span>

<span data-ttu-id="88ad2-130">KÜRZEN (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="88ad2-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="88ad2-131">Gibt 123 zurück.</span><span class="sxs-lookup"><span data-stu-id="88ad2-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="88ad2-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="88ad2-132">Example 3</span></span>

<span data-ttu-id="88ad2-133">KÜRZEN (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="88ad2-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="88ad2-134">Gibt 120 zurück.</span><span class="sxs-lookup"><span data-stu-id="88ad2-134">Returns 120.</span></span>
  

