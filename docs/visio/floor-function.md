---
title: FLOOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von Vielfaches.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797020"
---
# <a name="floor-function"></a><span data-ttu-id="46ea0-103">FLOOR Function</span><span class="sxs-lookup"><span data-stu-id="46ea0-103">FLOOR Function</span></span>

<span data-ttu-id="46ea0-104">Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von _Vielfaches_.</span><span class="sxs-lookup"><span data-stu-id="46ea0-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="46ea0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46ea0-105">Syntax</span></span>

<span data-ttu-id="46ea0-106">FLOOR (** *Anzahl* **, ** *mehrere* **)</span><span class="sxs-lookup"><span data-stu-id="46ea0-106">FLOOR(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="46ea0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ea0-107">Parameters</span></span>

|<span data-ttu-id="46ea0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="46ea0-108">**Name**</span></span>|<span data-ttu-id="46ea0-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="46ea0-109">**Required/Optional**</span></span>|<span data-ttu-id="46ea0-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="46ea0-110">**Data Type**</span></span>|<span data-ttu-id="46ea0-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46ea0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="46ea0-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="46ea0-112">_number_</span></span> <br/> |<span data-ttu-id="46ea0-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="46ea0-113">Required</span></span>  <br/> |<span data-ttu-id="46ea0-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="46ea0-114">**Number**</span></span> <br/> |<span data-ttu-id="46ea0-115">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="46ea0-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="46ea0-116">_mehrere_</span><span class="sxs-lookup"><span data-stu-id="46ea0-116">_multiple_</span></span> <br/> |<span data-ttu-id="46ea0-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="46ea0-117">Required</span></span>  <br/> |<span data-ttu-id="46ea0-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="46ea0-118">**Number**</span></span> <br/> |<span data-ttu-id="46ea0-119">Das Vielfache, auf das gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="46ea0-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="46ea0-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="46ea0-120">Return value</span></span>

<span data-ttu-id="46ea0-121">Zahl</span><span class="sxs-lookup"><span data-stu-id="46ea0-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46ea0-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46ea0-122">Remarks</span></span>

<span data-ttu-id="46ea0-123">Wenn _mehrere_ nicht angegeben ist, wird die Zahl in Richtung 0 auf die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="46ea0-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="46ea0-124">_Anzahl_ und _Vielfaches_ müssen die gleichen Vorzeichen oder ein #NUM haben.</span><span class="sxs-lookup"><span data-stu-id="46ea0-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="46ea0-125">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46ea0-125">error is returned.</span></span> <span data-ttu-id="46ea0-126">Wenn _Zahl_ oder _mehrere_ auf einen Wert, der ein #VALUE konvertiert werden kann!</span><span class="sxs-lookup"><span data-stu-id="46ea0-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="46ea0-127">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46ea0-127">error is returned.</span></span> <span data-ttu-id="46ea0-128">Wenn _Zahl_ oder _mehrere_ 0 ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="46ea0-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="46ea0-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46ea0-129">Example 1</span></span>

<span data-ttu-id="46ea0-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="46ea0-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="46ea0-131">Gibt 3 zurück.</span><span class="sxs-lookup"><span data-stu-id="46ea0-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="46ea0-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="46ea0-132">Example 2</span></span>

<span data-ttu-id="46ea0-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="46ea0-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="46ea0-134">Gibt -3 zurück.</span><span class="sxs-lookup"><span data-stu-id="46ea0-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="46ea0-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="46ea0-135">Example 3</span></span>

<span data-ttu-id="46ea0-136">FLOOR (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="46ea0-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="46ea0-137">Gibt 3,5 zurück.</span><span class="sxs-lookup"><span data-stu-id="46ea0-137">Returns 3.5.</span></span>
  

