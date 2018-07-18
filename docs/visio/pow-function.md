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
description: Gibt eine Zahl, die potenziert mit einem Exponenten zurück.
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797724"
---
# <a name="pow-function"></a><span data-ttu-id="f9c8e-103">POW Function</span><span class="sxs-lookup"><span data-stu-id="f9c8e-103">POW Function</span></span>

<span data-ttu-id="f9c8e-104">Gibt eine Zahl, die potenziert mit einem Exponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f9c8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9c8e-105">Syntax</span></span>

<span data-ttu-id="f9c8e-106">POW (** *Anzahl* **, ** *Exponent* **)</span><span class="sxs-lookup"><span data-stu-id="f9c8e-106">POW(** *number* **, ** *exponent* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f9c8e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9c8e-107">Parameters</span></span>

|<span data-ttu-id="f9c8e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-108">**Name**</span></span>|<span data-ttu-id="f9c8e-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-109">**Required/Optional**</span></span>|<span data-ttu-id="f9c8e-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-110">**Data Type**</span></span>|<span data-ttu-id="f9c8e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f9c8e-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="f9c8e-112">_number_</span></span> <br/> |<span data-ttu-id="f9c8e-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f9c8e-113">Required</span></span>  <br/> |<span data-ttu-id="f9c8e-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-114">**Number**</span></span> <br/> |<span data-ttu-id="f9c8e-115">Die Zahl, die mit einem Exponenten potenziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="f9c8e-116">_exponent_</span><span class="sxs-lookup"><span data-stu-id="f9c8e-116">_exponent_</span></span> <br/> |<span data-ttu-id="f9c8e-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f9c8e-117">Required</span></span>  <br/> |<span data-ttu-id="f9c8e-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="f9c8e-118">**Number**</span></span> <br/> |<span data-ttu-id="f9c8e-119">Der Exponent.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9c8e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9c8e-120">Remarks</span></span>

<span data-ttu-id="f9c8e-121">_Zahl_ und _Exponent_ können keine ganzen Zahlen sein und kann einen negativen Wert haben.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="f9c8e-122">Wenn _Zahl_ nicht gleich 0 und _Exponent_ ist 0, diese Funktion gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="f9c8e-123">Wenn _Zahl_ 0 gleich und _Exponent_ negativ ist, gibt diese Funktion 0,0 zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="f9c8e-124">Wenn _Zahl_ und _Exponent_ 0 sind oder _Zahl_ negativ und _Exponent_ ist keine Ganzzahl ist, gibt diese Funktion 0,0 zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="f9c8e-125">Wenn _Zahl_ und _Exponent_ negativ sind, gibt diese Funktion-1 zurück. #IND.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f9c8e-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f9c8e-126">Example</span></span>

<span data-ttu-id="f9c8e-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="f9c8e-127">POW(5,2)</span></span> 
  
<span data-ttu-id="f9c8e-128">Gibt 25 zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c8e-128">Returns 25.</span></span> 
  

