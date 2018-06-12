---
title: OR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke als Parameter übergebene wahr sind.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797571"
---
# <a name="or-function"></a><span data-ttu-id="641b9-103">OR Function</span><span class="sxs-lookup"><span data-stu-id="641b9-103">OR Function</span></span>

<span data-ttu-id="641b9-104">Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke als Parameter übergebene wahr sind.</span><span class="sxs-lookup"><span data-stu-id="641b9-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="641b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="641b9-105">Syntax</span></span>

<span data-ttu-id="641b9-106">ODER (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *LogicalexpressionN* **)</span><span class="sxs-lookup"><span data-stu-id="641b9-106">OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="641b9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="641b9-107">Parameters</span></span>

|<span data-ttu-id="641b9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="641b9-108">**Name**</span></span>|<span data-ttu-id="641b9-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="641b9-109">**Required/Optional**</span></span>|<span data-ttu-id="641b9-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="641b9-110">**Data Type**</span></span>|<span data-ttu-id="641b9-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="641b9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="641b9-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="641b9-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="641b9-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="641b9-113">Required</span></span>  <br/> |<span data-ttu-id="641b9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="641b9-114">**String**</span></span> <br/> |<span data-ttu-id="641b9-115">Der erste Ausdruck, dessen Wahrheit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="641b9-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="641b9-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="641b9-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="641b9-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="641b9-117">Required</span></span>  <br/> |<span data-ttu-id="641b9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="641b9-118">**String**</span></span> <br/> |<span data-ttu-id="641b9-119">Der zweite Ausdruck, dessen Wahrheit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="641b9-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="641b9-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="641b9-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="641b9-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="641b9-121">Required</span></span>  <br/> |<span data-ttu-id="641b9-122">**String**</span><span class="sxs-lookup"><span data-stu-id="641b9-122">**String**</span></span> <br/> |<span data-ttu-id="641b9-123">Der n-te Ausdruck, dessen Wahrheit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="641b9-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="641b9-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="641b9-124">Return value</span></span>

<span data-ttu-id="641b9-125">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="641b9-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="641b9-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="641b9-126">Remarks</span></span>

<span data-ttu-id="641b9-p101">Ein beliebiger Ausdruck, der einen Wert ungleich Null ergibt, wird als TRUE betrachtet. Wenn alle logischen Ausdrücke den Wert FALSE oder 0 aufweisen, gibt die Funktion FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="641b9-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="641b9-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="641b9-129">Example</span></span>

<span data-ttu-id="641b9-130">ODER (Höhe \> 1, DrehbezX \> 1)</span><span class="sxs-lookup"><span data-stu-id="641b9-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="641b9-p102">Gibt TRUE (1) zurück, wenn mindestens einer der beiden Ausdrücke TRUE ist. Gibt FALSE (0) zurück, wenn beide Ausdrücke FALSE sind.</span><span class="sxs-lookup"><span data-stu-id="641b9-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

