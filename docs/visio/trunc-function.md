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
description: Gibt eine Zahl auf die angegebene Anzahl von Ziffern gekürzt.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798311"
---
# <a name="trunc-function"></a><span data-ttu-id="13f07-103">TRUNC Function</span><span class="sxs-lookup"><span data-stu-id="13f07-103">TRUNC Function</span></span>

<span data-ttu-id="13f07-104">Gibt eine Zahl auf die angegebene Anzahl von Ziffern gekürzt.</span><span class="sxs-lookup"><span data-stu-id="13f07-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="13f07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13f07-105">Syntax</span></span>

<span data-ttu-id="13f07-106">TRUNC (** *Anzahl* **, ** *AnzahlVonStellen* **)</span><span class="sxs-lookup"><span data-stu-id="13f07-106">TRUNC(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="13f07-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="13f07-107">Parameters</span></span>

|<span data-ttu-id="13f07-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="13f07-108">**Name**</span></span>|<span data-ttu-id="13f07-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="13f07-109">**Required/Optional**</span></span>|<span data-ttu-id="13f07-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="13f07-110">**Data Type**</span></span>|<span data-ttu-id="13f07-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13f07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="13f07-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="13f07-112">_number_</span></span> <br/> |<span data-ttu-id="13f07-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="13f07-113">Required</span></span>  <br/> |<span data-ttu-id="13f07-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="13f07-114">**Numeric**</span></span> <br/> |<span data-ttu-id="13f07-115">Die zu kürzende Zahl.</span><span class="sxs-lookup"><span data-stu-id="13f07-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="13f07-116">_AnzahlVonStellen_</span><span class="sxs-lookup"><span data-stu-id="13f07-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="13f07-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="13f07-117">Required</span></span>  <br/> |<span data-ttu-id="13f07-118">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="13f07-118">**Numeric**</span></span> <br/> |<span data-ttu-id="13f07-119">Die Anzahl der Ziffern an die zu kürzende _Zahl_.</span><span class="sxs-lookup"><span data-stu-id="13f07-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="13f07-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="13f07-120">Return value</span></span>

<span data-ttu-id="13f07-121">Numeric.</span><span class="sxs-lookup"><span data-stu-id="13f07-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13f07-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13f07-122">Remarks</span></span>

<span data-ttu-id="13f07-123">Wenn _AnzahlVonStellen_ größer als 0 ist, wird _Zahl_ auf die rechts vom Dezimalkomma _AnzahlVonStellen_ gekürzt.</span><span class="sxs-lookup"><span data-stu-id="13f07-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="13f07-124">Wenn _AnzahlVonStellen_ 0 ist, wird _Zahl_ auf eine ganze Zahl gekürzt.</span><span class="sxs-lookup"><span data-stu-id="13f07-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="13f07-125">Wenn _AnzahlVonStellen_ kleiner als 0 ist, wird _Zahl_ auf die links vom Dezimalkomma _AnzahlVonStellen_ gekürzt.</span><span class="sxs-lookup"><span data-stu-id="13f07-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="13f07-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13f07-126">Example 1</span></span>

<span data-ttu-id="13f07-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="13f07-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="13f07-128">Gibt 123,65 zurück.</span><span class="sxs-lookup"><span data-stu-id="13f07-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="13f07-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="13f07-129">Example 2</span></span>

<span data-ttu-id="13f07-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="13f07-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="13f07-131">Gibt 123 zurück.</span><span class="sxs-lookup"><span data-stu-id="13f07-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="13f07-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="13f07-132">Example 3</span></span>

<span data-ttu-id="13f07-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="13f07-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="13f07-134">Gibt 120 zurück.</span><span class="sxs-lookup"><span data-stu-id="13f07-134">Returns 120.</span></span>
  

