---
title: POW-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Gibt eine Zahl zurück, die auf die Macht eines Exponenten angehoben wird.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406311"
---
# <a name="pow-function"></a><span data-ttu-id="65c2f-103">POW Function</span><span class="sxs-lookup"><span data-stu-id="65c2f-103">POW Function</span></span>

<span data-ttu-id="65c2f-104">Gibt eine Zahl zurück, die auf die Macht eines Exponenten angehoben wird.</span><span class="sxs-lookup"><span data-stu-id="65c2f-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="65c2f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65c2f-105">Syntax</span></span>

<span data-ttu-id="65c2f-106">POW(\*\* *Number* \*\*, \*\* *exponent* \*\* )</span><span class="sxs-lookup"><span data-stu-id="65c2f-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="65c2f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="65c2f-107">Parameters</span></span>

|<span data-ttu-id="65c2f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="65c2f-108">**Name**</span></span>|<span data-ttu-id="65c2f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="65c2f-109">**Required/Optional**</span></span>|<span data-ttu-id="65c2f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="65c2f-110">**Data Type**</span></span>|<span data-ttu-id="65c2f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65c2f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="65c2f-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="65c2f-112">_number_</span></span> <br/> |<span data-ttu-id="65c2f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="65c2f-113">Required</span></span>  <br/> |<span data-ttu-id="65c2f-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="65c2f-114">**Number**</span></span> <br/> |<span data-ttu-id="65c2f-115">Die Zahl, die mit einem Exponenten potenziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65c2f-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="65c2f-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="65c2f-116">_exponent_</span></span> <br/> |<span data-ttu-id="65c2f-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="65c2f-117">Required</span></span>  <br/> |<span data-ttu-id="65c2f-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="65c2f-118">**Number**</span></span> <br/> |<span data-ttu-id="65c2f-119">Der Exponent.</span><span class="sxs-lookup"><span data-stu-id="65c2f-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65c2f-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65c2f-120">Remarks</span></span>

<span data-ttu-id="65c2f-121">Sowohl  _Zahl_ als  _auch Exponent_ können nicht ganzzahlig sein, und sie können negativ sein.</span><span class="sxs-lookup"><span data-stu-id="65c2f-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="65c2f-122">Wenn  _Zahl_ nicht 0 und  _Exponent_ 0 ist, gibt diese Funktion 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="65c2f-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="65c2f-123">Wenn  _Zahl_ 0 und  _Exponent_ negativ ist, gibt diese Funktion 0,0 zurück.</span><span class="sxs-lookup"><span data-stu-id="65c2f-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="65c2f-124">Wenn Zahl _und_ _Exponent_ 0  sind oder Zahl negativ ist und _exponent_ keine ganze Zahl ist, gibt diese Funktion 0,0 zurück.</span><span class="sxs-lookup"><span data-stu-id="65c2f-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="65c2f-125">Wenn Zahl  _und_  _Exponent_ negativ sind, gibt diese Funktion -1,#IND.</span><span class="sxs-lookup"><span data-stu-id="65c2f-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="65c2f-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="65c2f-126">Example</span></span>

<span data-ttu-id="65c2f-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="65c2f-127">POW(5,2)</span></span> 
  
<span data-ttu-id="65c2f-128">Gibt 25 zurück.</span><span class="sxs-lookup"><span data-stu-id="65c2f-128">Returns 25.</span></span> 
  

